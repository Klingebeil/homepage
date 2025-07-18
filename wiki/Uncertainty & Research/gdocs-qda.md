---
layout: wikicrumb
title: Qualitative Analysis in Google Docs
first-commit: 2025-07-17
last-updated: 2025-07-17
---

# A Lightweight QDA Workflow with Google Docs and Sheets

This micro-tool lets you use Google Docs as a lightweight qualitative analysis platform. By tagging content with comments and pulling those into a Google Sheet, you can sort, filter, and analyze your data — collaboratively and for free..

This is a small project, updating [four year old code](https://stackoverflow.com/questions/66103464/export-google-docs-comments-into-google-sheets-along-with-highlighted-text/77175615#77175615) from Stack Overflow.

## How to implement it

1. Create a Google Doc and a Google Sheet
2. In the Google Sheet add the "Apps Script" extension. A new tab should open.
3. Under "Services" on the left side panel, add "Drive API"
4. Paste in the following code:

```
function listComments() {
  // Change docId into your document's ID
  var docId = 'YOUR DOC ID'; 
  
  // Add the required fields parameter
  var comments = Drive.Comments.list(docId, {
    fields: 'comments(content,quotedFileContent,anchor,author,deleted,id)',
    includeDeleted: false
  });
  
  var hList = [], cList = [], aList = [], lList = [];

  // Get list of comments
  if (comments.comments && comments.comments.length > 0) {
    for (var i = 0; i < comments.comments.length; i++) {
      var comment = comments.comments[i]; 
      
      // Skip deleted comments (extra safety check)
      if (comment.deleted) {
        continue;
      }
      
      // In Drive API v3, the structure is different
      // quotedFileContent contains the highlighted text
      var highlightedText = '';
      if (comment.quotedFileContent && comment.quotedFileContent.value) {
        highlightedText = comment.quotedFileContent.value;
      } else if (comment.anchor) {
        // anchor contains the selection info as a JSON string
        highlightedText = comment.anchor;
      }
      
      // content contains the actual comment text
      var commentText = comment.content || '';
      
      // author contains the author information
      var authorName = '';
      if (comment.author) {
        authorName = comment.author.displayName || comment.author.emailAddress || '';
      }
      
      // create direct link to comment
      var commentLink = 'https://docs.google.com/document/d/' + docId + '/edit#comment-' + comment.id;
      
      // add comment, highlight, author, and link to arrays
      hList.unshift([highlightedText]);
      cList.unshift([commentText]);
      aList.unshift([authorName]);
      lList.unshift([commentLink]);
    }
    // Set values to A, B, C, and D columns
    var sheet = SpreadsheetApp.getActiveSheet();
    sheet.getRange("A1:A" + hList.length).setValues(hList);
    sheet.getRange("B1:B" + cList.length).setValues(cList);
    sheet.getRange("C1:C" + aList.length).setValues(aList);
    sheet.getRange("D1:D" + lList.length).setValues(lList);
  }
}
```

5. Run the code. The first time the script will ask you for permission to access your files. Once granted, it should run without problems.

The output will look like this:

> | Text highlighted | Comment | Author of Comment | Link to Comment |

## Limitations
- the script only works if: a) you have permission to read comments on the Doc and b) the Doc is accessible from the account running the script
- The script will grab all comments, excluding only deleted ones—meaning the only way to exclude a comment is to truly delete it in the docoument
- The script will not update live but only when executed, meaning changes made in the Google Sheet might get lost when executed again
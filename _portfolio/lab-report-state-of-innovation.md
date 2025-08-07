---
layout: portfolio
title: "Lab Report: State of Innovation"
date: 2024-02-01
category: Research
teaser-img: portfolio/lab-report-innovation/report-workspace.png
summary: "A report on contemporary innovation practices inside German media companies."
published: true
toc: true
---

# Lab Report: State of Innovation

{% include img-full.html path="portfolio/lab-report-innovation/report-workspace.png" %}

## What was the challenge?

**Together with my colleague [Christian Simon](https://www.linkedin.com/in/christian-simon-b41b32102/), we had set ourselves the goal of drawing a cross-section of the state of innovation work in German media companies. What does innovation actually look like in practice? How is it supported? Do innovation methods even work at all?**

We were able to build on our experience with the *[Lab Report: Künstliche Intelligenz](https://johannesklingebiel.de/portfolio/lab-report-kuenstliche-intelligenz)*, but it was clear from the start that the research and analysis would be more complex this time.

## Survey & Interviews

For this research, we used a mixed-methods approach by combining a quantitative survey with follow-up and expert interviews.

To recruit participants in media companies, we drew on several *Hubspot* lists of the *Media Lab Bayern* that contained our likely audience: readers of previous reports, people who had applied to relevant grant programs and attended events geared towards media companies. We were looking for media professionals who were involved in "innovation work" without necessarily working in an institutionalised innovation team.

We chose *Typeform* for the questionnaire itself for two reasons:

- *Typeform* offered the possibility to use so-called “branches”, i.e. to ask additional questions based on previous answers. We were therefore able to ask automated follow-up questions.
- We were also able to use the Media Lab design for *Typeform* for a more appealing survey design than would have been possible with *Google Forms*, for example. A nice-to-have.

In complement to our quantitative survey, we conducted qualitative interviews to shed light on edge cases. We recruited participants directly from the survey by asking for their consent to contact them for further questioning. These interviews provided valuable insights into the perspectives, experiences, and challenges faced by industry professionals. We also conducted four domain expert interviews with Anita Zielina, Katharina Köth, Stefan Ottlitz, and Johannes Kleske. All interviews were conducted and recorded using *Zoom*. 

During the interviews, we deliberately confronted participants with findings from the quantitative survey, as to include multiple perspectives and challenge our assumption about the data. This iterative process allowed us to refine our understanding of key themes and validate our interpretations against real-world experiences.

### Analysis & evaluation

The 104 participants in our survey resulted in almost 5880 data points, crammed into an *Excel* sheet. Given the nature of our research and the relatively modest sample size, we opted for a straightforward approach to data analysis, focusing on identifying key trends and intersections within the dataset. 

While more complex statistical methods were available, we made a deliberate decision not to employ them due to the size of our dataset and the exploratory nature of our research. Instead, our focus was on identifying patterns, correlations, and thematic clusters within the responses.

{% include img-full.html path="portfolio/lab-report-innovation/google-sheet.png" %}

### Evaluating qualitative data with AI

We transcribed the interviews with *MacWhisper*, a small program that runs OpenAI's Whisper model offline. The large model (3GB) takes about 5 minutes for 30 minutes of audio on a MacBook Pro and is surprisingly accurate, but cannot automatically distinguish between two speakers. So each transcript needed some fine-tuning (about 1 hour per interview).

To extract content from the interviews, we experimented with two tools: *ChatGPT* and *[Notably](https://www.notably.ai/)*.

- *Notably* — Built for qualitative research, you can upload interviews, mark and cluster text passages and use GPT to generate initial summaries and reports. It works okay-ish. Good enough for a first start, but not perfect and suffers from all known problems of large language models. It might work a bit better with more content to work from, though.
- *ChatGPT* — Somewhat more helpful were summaries of the individual interviews, created by the free ChatGPT version. Here, too, cross-referencing was necessary, but the results were helpful in getting a better picture of the topics discussed and helped in pulling together the chapters across multiple data sources.

## Write, write, write

As with the [Lab Report: Künstliche Intelligenz](https://johannesklingebiel.de/portfolio/lab-report-kuenstliche-intelligenz), we used the following tools to help us structure the work:

- A flat plan in *Miro* to track layout changes and plan the various chapters throughout the report
- A *Google Docs* spreadsheet to track the progress of individual texts

{% include img-full.html path="portfolio/lab-report-innovation/miro-flatplan.png" info="A screenshot of the flatplan with parts of the layout already finished" %}

We clustered the data from the interviews and the survey around a couple of emerging topics—some we had anticipated in the survey design, others emerged during the research:

- The role of the management in enabling and hindering innovation initiatives, especially the challenges of navigating projects through hierarchies and hidden power structures.
- The setup and goals of innovation initiatives across different media companies and the differences and similarities in how they approached innovation initiatives.
- The use of so-called “innovation methods” and where they worked and failed, with a focus on Design Thinking.

In the end, the report comprised 19 pages and 50,000 characters of text.

## What we learned

1. **The critical perspective was valuable**—This was one of the main feedback from readers: taking a more critical perspective helped in building credibility for the *Media Lab Bayern*, especially if we manage to remain balanced (a good example here is the critical Design Thinking chapter in the report)
2. **Layout & Design**—The grid layout, which I developed for the [Lab Report: Künstliche Intelligenz](https://johannesklingebiel.de/portfolio/lab-report-kuenstliche-intelligenz), not only worked well for this report, but was also easy to adapt to the content with a few tongue-in-cheek elements.
3. **Automatic feedback e-mail**—The extended Hubspot workflow with an automatic request for feedback seven days after a download was not very fruitful, but still helpful. An interest in “innovative business models” was mentioned several times in the feedback — a possible follow-up topic.
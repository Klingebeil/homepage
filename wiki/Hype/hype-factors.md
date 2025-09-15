---
layout: wikicrumb
title: Hype-o-mat
first-commit: 2025-09-15
last-updated: 2025-09-15
linked-notes:
- permissive-uncertainty
- 02-sociology-of-expectations
---

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hype Factor Calculator</title>
    <style>
        .factor {
            margin: 1em 0;
            padding: 20px;
            background: white;
            border-radius: 12px;
        }
        
        .factor-name {
            padding: 0;
            margin: 0 !important;
        }
        
        .factor-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .slider-container {
            margin: 15px 0;
        }
        
        .slider {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: var(--background);
            outline: none;
            -webkit-appearance: none;
            cursor: pointer;
        }
        
        .slider-labels {
            display: flex;
            justify-content: space-between;
            margin-top: 8px;
            font-size: 0.85rem;
            color: var(--dark-grey);
        }
        
        .less-permissive {
            text-align: left;
            flex: 1;
        }
        
        .more-permissive {
            text-align: right;
            flex: 1;
        }
        
        .examples {
            margin-top: 10px;
            padding: 10px;
            background: var(--light-grey);
            border-radius: 8px;
            font-size: 0.9rem;
            color: #5f6368;
            font-style: italic;
        }
        
        .result {
            background: var(--white);
            color: var(--main-txt-color);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            margin-top: 30px;
        }
        
        .hype-score {
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 10px;
        }
        
        .hype-label {
            font-size: 1.5rem;
            margin-bottom: 15px;
            opacity: 0.9;
        }
        
        .hype-description {
            font-size: 1rem;
            opacity: 0.8;
            line-height: 1.5;
        }
    </style>
</head>
<body>
    <h1>Hype-o-mat</h1>
    <p>A handy tool to check how likely hyped-up claims might be encountered in your current environment.</p>
    <div class="category">
        <h2>Epistemic Infrastructure</h2>        
        <div class="factor hairline">
            <div class="factor-header">
                <h3 class="factor-name">How easily are the claims quantifiable?</h3>
            </div>
            <div class="slider-container">
                <input type="range" min="1" max="5" value="3" class="slider" id="measurement-slider">
                <div class="slider-labels">
                    <span class="less-permissive">Clear, objective measurements available</span>
                    <span class="more-permissive">Outcomes hard to quantify; subjective metrics</span>
                </div>
            </div>
            <div class="examples">Processor speed improvements vs. AI consciousness</div>
        </div>         
        <div class="factor hairline">
            <div class="factor-header">
                <h3 class="factor-name">How distant are the predictions made?</h3>
            </div>
            <div class="slider-container">
                <input type="range" min="1" max="5" value="3" class="slider" id="temporal-slider">
                <div class="slider-labels">
                    <span class="less-permissive">Near-term forecasts</span>
                    <span class="more-permissive">Distant future predictions</span>
                </div>
            </div>
            <div class="examples">Next week's weather vs. Climate predictions for 2100</div>
        </div>      
        <div class="factor hairline">
            <div class="factor-header">
                <h3 class="factor-name">How many fields or disciplines are involved?</h3>
            </div>
            <div class="slider-container">
                <input type="range" min="1" max="5" value="3" class="slider" id="disciplinary-slider">
                <div class="slider-labels">
                    <span class="less-permissive">Single disciplinary authority</span>
                    <span class="more-permissive">Interdisciplinary/boundary topics</span>
                </div>
            </div>
            <div class="examples">Pure mathematics vs. computational neuroscience</div>
        </div>
    </div>
    <div class="category">
        <h2 class="category-title">Social & Institutional</h2>
        <div class="factor hairline">
            <div class="factor-header">
                <h3 class="factor-name">Who is the audience?</h3>
            </div>
            <div class="slider-container">
                <input type="range" min="1" max="5" value="3" class="slider" id="audience-slider">
                <div class="slider-labels">
                    <span class="less-permissive">Homogeneous specialist communities</span>
                    <span class="more-permissive">Heterogeneous expert-lay mixtures</span>
                </div>
            </div>
            <div class="examples">Peer review panels vs. TED talks</div>
        </div>
        <div class="factor hairline">
            <div class="factor-header">
                <h3 class="factor-name">What are people rewarded for?</h3>
            </div>
            <div class="slider-container">
                <input type="range" min="1" max="5" value="3" class="slider" id="incentives-slider">
                <div class="slider-labels">
                    <span class="less-permissive">Penalties for false positives</span>
                    <span class="more-permissive">Rewards for bold predictions</span>
                </div>
            </div>
            <div class="examples">Medical device approval vs. Venture capital pitches</div>
        </div>
        <div class="factor hairline">
            <div class="factor-header">
                <h3 class="factor-name">How quickly does information spread?</h3>
            </div>
            <div class="slider-container">
                <input type="range" min="1" max="5" value="3" class="slider" id="media-slider">
                <div class="slider-labels">
                    <span class="less-permissive">Controlled information flow</span>
                    <span class="more-permissive">Fast circulation, slow verification</span>
                </div>
            </div>
            <div class="examples">Academic journals vs. social media</div>
        </div>
    </div>
    <div class="category">
        <h2 class="category-title">Rhetorical & Cultural</h2>
        <div class="factor hairline">
            <div class="factor-header">
                <h3 class="factor-name">How novel are the claims made?</h3>
            </div>
            <div class="slider-container">
                <input type="range" min="1" max="5" value="3" class="slider" id="analogical-slider">
                <div class="slider-labels">
                    <span class="less-permissive">Novel concepts without precedent</span>
                    <span class="more-permissive">Claims supported by familiar analogies</span>
                </div>
            </div>
            <div class="examples">Quantum computing vs. "AI is like a brain"</div>
        </div>
        <div class="factor hairline">
            <div class="factor-header">
                <h3 class="factor-name">Does the speaker align with common beliefs?</h3>
            </div>
            <div class="slider-container">
                <input type="range" min="1" max="5" value="3" class="slider" id="cultural-slider">
                <div class="slider-labels">
                    <span class="less-permissive">Conflicts with cultural expectations</span>
                    <span class="more-permissive">Aligns with deep cultural narratives</span>
                </div>
            </div>
            <div class="examples">Anti-progress sentiments vs. Technological salvation</div>
        </div>
        <div class="factor hairline">
            <div class="factor-header">
                <h3 class="factor-name">Does the speaker borrow credibility from famous sources?</h3>
            </div>
            <div class="slider-container">
                <input type="range" min="1" max="5" value="3" class="slider" id="credibility-slider">
                <div class="slider-labels">
                    <span class="less-permissive">Standalone claims from unknown sources</span>
                    <span class="more-permissive">Association with prestigious sources</span>
                </div>
            </div>
            <div class="examples">Anonymous blogger vs. MIT researcher</div>
        </div>
    </div>
    <div class="result shadow-green">
        <div class="hype-label" id="hype-label"></div>
        <div class="mono-space centered small color-dark-gray" id="hype-description"></div>
    </div>

<script>
    function updateHypeFactor() {
        const measurement = parseInt(document.getElementById('measurement-slider').value);
        const temporal = parseInt(document.getElementById('temporal-slider').value);
        const disciplinary = parseInt(document.getElementById('disciplinary-slider').value);
        const audience = parseInt(document.getElementById('audience-slider').value);
        const incentives = parseInt(document.getElementById('incentives-slider').value);
        const media = parseInt(document.getElementById('media-slider').value);
        const analogical = parseInt(document.getElementById('analogical-slider').value);
        const cultural = parseInt(document.getElementById('cultural-slider').value);
        const credibility = parseInt(document.getElementById('credibility-slider').value);

        // Calculate category scores
        const epistemicScore = measurement + temporal + disciplinary;
        const socialScore = audience + incentives + media;
        const rhetoricalScore = analogical + cultural + credibility;
        const totalScore = epistemicScore + socialScore + rhetoricalScore;

        // Update hype level and description
        let hypeLabel, hypeDescription;
        if (totalScore <= 15) {
            hypeLabel = "Low Hype Risk";
            hypeDescription = "Conditions strongly favor careful, evidence-based predictions";
        } else if (totalScore <= 30) {
            hypeLabel = "Moderate Hype Risk";
            hypeDescription = "Mixed conditions with some factors favoring overconfidence";
        } else if (totalScore <= 35) {
            hypeLabel = "High Hype Risk";
            hypeDescription = "Multiple conditions align to encourage bold, unverified claims";
        } else if (totalScore <= 40) {
            hypeLabel = "Very High Hype Risk";
            hypeDescription = "Perfect storm conditions for hype and overconfident predictions";
        } else {
            hypeLabel = "Extreme Hype Risk";
            hypeDescription = "Maximum hype conditions — expect wild, unsubstantiated claims";
        }

        document.getElementById('hype-label').textContent = hypeLabel;
        document.getElementById('hype-description').textContent = hypeDescription;
    }

    // Add event listeners to all sliders
    document.querySelectorAll('.slider').forEach(slider => {
        slider.addEventListener('input', updateHypeFactor);
    });

    // Initialize
    updateHypeFactor();
</script>
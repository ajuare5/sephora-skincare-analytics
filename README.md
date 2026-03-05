# Sephora Skincare Sentiment Analytics

NLP pipeline for analyzing 87,832 Sephora customer reviews across 153 products and 67+ brands. Builds a custom attribute lexicon to identify key product features, scores sentiment at the sentence level, and measures brand-level attribute lift to reveal what drives positive and negative perception.

[View Report](report.pdf)

## Team
- Arturo Juarez Jr.
- Abhilash Bagde
- Bakr Katkhuda
- Luke Hartfield
- Mihir Jeshurun Gandham
- Vedant Mehrotra

## Methodology

**1. Attribute Lexicon Construction**
- 40+ skincare attributes organized into categories: cleansing, moisture balance, sensory qualities, skin reactions, results, usability/value
- Regex-based pattern matching with negation detection

**2. Sentiment Scoring**
- Hybrid approach: star rating as weak prior + positive/negative lexicon matching
- Sentence-level polarity scoring with helpful vote weighting

**3. Lift Analysis**
- Log₂ likelihood ratio: P(attribute | brand) vs. P(attribute | global)
- Identifies which attributes are disproportionately associated with each brand
- Cross-tabulated by brand × skin type

## Key Outputs
- Top 5 positive and negative attributes ranked by lift per brand
- Net sentiment scores for brand-attribute pairs
- Skin-type-specific brand profiles (oily, dry, combination, sensitive)

## Repository Structure
```
├── sephora_sentiment_analysis.ipynb    # Full pipeline (lexicon → sentiment → lift scoring)
└── report.pdf                          # Final project report
```

> **Note:** Dataset not included. Source: Sephora product reviews dataset (87,832 reviews, available on Kaggle).

## Technologies
- Python, pandas, NumPy, re (regex), Matplotlib, custom NLP (no external NLP libraries)

## Course
Advanced Data Mining & Web Analytics — UT Austin McCombs School of Business

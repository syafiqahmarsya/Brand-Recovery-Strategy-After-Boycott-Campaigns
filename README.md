# Brand Recovery Strategy After Boycott Campaigns Through Social Media Sentiment Analysis

## Project Overview

This project analyzes public sentiment and online discussions surrounding consumer boycott campaigns against brands associated with Israel, using YouTube comments.

The objective is to understand public perceptions, identify key issues driving boycott discussions, analyze sentiment trends, and develop data-driven business recommendations to help companies rebuild brand trust and mitigate reputational risks.

The project combines sentiment analysis, exploratory data analysis (EDA), text mining, and topic modeling to transform unstructured social media data into actionable business insights.

## Project Objectives

- Analyze public sentiment toward brands affected by boycott campaigns.
- Identify trends and patterns in online discussions.
- Explore key topics and issues driving boycott-related conversations.
- Examine public perceptions of brand reputation and consumer alternatives.
- Develop business recommendations and scenario-based revenue projections.

## Dataset

| Information | Description |
|---|---|
| Data Source | YouTube Comments |
| Data Period | October 17, 2023 – July 15, 2025 |
| Total Comments | 6,102 |
| Keywords | 8 boycott-related hashtags |
| Language | Indonesian |

**Keywords Used:**
- #produkisrael
- #boikotprodukisrael
- #aksiboikot
- #penggantiprodukisrael
- #boikotkfc
- #boikotunilever
- #boikotstarbuck
- #dampakboikot

## Tools & Technologies

- **Python:** Data processing and analysis
- **Pandas & NumPy:** Data manipulation
- **Matplotlib & Seaborn:** Data visualization
- **NLTK:** Text preprocessing and tokenization
- **Sastrawi:** Indonesian text stemming
- **Scikit-learn:** Text feature extraction
- **NetworkX:** Bigram network analysis
- **WordCloud:** Text visualization
- **BERTopic:** Topic modeling
- **UMAP & HDBSCAN:** Dimensionality reduction and clustering

## Methodology

### 1. Data Collection
- Collected YouTube comments using the YouTube Data API.
- Used eight boycott-related hashtags to identify relevant discussions.
- Combined datasets and removed duplicate comments.

### 2. Data Preprocessing
- Removed irrelevant comments, including non-Indonesian and online gambling-related content.
- Performed sentiment labeling into three categories:
  - **Positive:** Comments supporting the use of boycotted products.
  - **Neutral:** Comments expressing neutral opinions or discussions.
  - **Negative:** Comments opposing the use of boycotted products.
- Handled duplicate records and missing values.
- Applied text cleaning, normalization, stopword removal, stemming using Sastrawi, and tokenization.

### 3. Exploratory Data Analysis (EDA)

Analyzed:
- Sentiment distribution across keywords.
- Most frequently discussed boycott-related keywords.
- Monthly trends in comment volume.
- Distribution of negative sentiment by keyword.
- Duration of discussions for each keyword.

### 4. Text Analysis
- Used WordCloud to identify frequently occurring words.
- Applied bigram network analysis to explore relationships between frequently co-occurring words.
- Used NetworkX to examine word connections and degree centrality.

### 5. Topic Modeling

Applied BERTopic to identify discussion themes within positive, neutral, and negative sentiment groups.

The analysis incorporated:
- UMAP for dimensionality reduction.
- HDBSCAN for clustering.
- BERTopic for topic extraction and interpretation.

## Key Findings & Business Insights

### 1. Neutral and Negative Sentiment Dominated Public Discussions

Neutral sentiment accounted for 43.5% of comments, followed by negative sentiment at 32.7% and positive sentiment at 23.8%.

This indicates that public discussions were largely characterized by neutral opinions and opposition toward the use of boycotted products.

### 2. Boycott Campaigns Encouraged Interest in Local Products

Discussions highlighted local products and UMKM as alternatives to brands associated with boycott campaigns.

### 3. Neutral Consumers Focused on Price and Product Alternatives

Neutral discussions frequently revolved around product prices, quality, and alternative purchasing options rather than direct support or opposition to boycott campaigns.

### 4. Economic Concerns Emerged Across Different Sentiment Groups

Discussions included concerns about the potential impact of boycotts on local businesses, employees, and UMKM.

### 5. Public Attention Varied Across Keywords and Time Periods

Some keywords maintained discussion activity over a longer period, while others experienced temporary increases, particularly around November–December 2023.

## Scenario-Based Revenue Projection

A scenario-based revenue projection was developed to illustrate the potential business implications of sentiment distribution for KFC.

The simulation used the following assumptions:

| Sentiment Category | Assumption |
|---|---|
| Positive | 100% retained as loyal customers |
| Neutral | 10%, 15%, and 20% potentially return as customers |
| Negative | 5% potentially return as customers |
| Average Transaction Value | IDR 50,000 per customer per day |

The analysis explored several customer recovery scenarios based on different conversion assumptions for neutral sentiment groups.

**Note:** This projection represents an illustrative business scenario based on assumptions, not an actual sales forecast. Social media sentiment data does not directly measure verified customer purchasing behavior.

## Business Recommendations

Based on the findings, several strategies were proposed:

- **Rebuild Brand Trust:** Develop transparent communication to address public concerns.
- **Strengthen Brand Communication:** Clarify the brand's position and respond to public discussions.
- **Improve Product Competitiveness:** Evaluate product quality, pricing, and value propositions.
- **Implement Promotional Strategies:** Use promotions and soft-selling approaches to attract price-conscious consumers.
- **Collaborate with Local Businesses:** Build partnerships with UMKM and communicate the positive social impact of these collaborations.
- **Restore Brand Reputation:** Take advantage of declining public attention to strengthen brand image and consumer trust.

## Project Outcome

This project demonstrates how social media analytics and text mining can be used to understand public perceptions during boycott campaigns.

By combining sentiment analysis, topic modeling, and scenario-based business projections, the analysis translates unstructured online discussions into actionable insights and strategic recommendations for brand reputation management.

## Project Information

**Project Type:** Collaborative Capstone Project

**Domain:** Data Analytics | Social Media Analytics | Sentiment Analysis | Text Mining | Topic Modeling

**Contribution:** Data collection, sentiment labeling, data preprocessing, exploratory data analysis, text visualization, insight development, and business recommendations.

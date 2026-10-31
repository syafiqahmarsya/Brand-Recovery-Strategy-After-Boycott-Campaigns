# Brand Recovery Strategy After Boycott Campaigns Through Social Media Sentiment Analysis

## Project Overview

This project analyzes public sentiment and online discussions surrounding consumer boycott campaigns against brands associated with Israel, using YouTube comments.

The project aims to understand how public perceptions develop during boycott campaigns, identify the main issues driving online discussions, examine sentiment trends, and provide business insights and recommendations to help companies mitigate reputational risks and rebuild consumer trust.

The analysis combines social media analytics, sentiment analysis, exploratory data analysis (EDA), text mining, and topic modeling to transform unstructured social media comments into actionable business insights.

## Project Objectives

- Analyze public sentiment toward products and brands affected by boycott campaigns.
- Identify trends and patterns in boycott-related discussions across different keywords.
- Explore the main topics and issues emerging from online conversations.
- Understand public perceptions of boycotted products and local alternatives.
- Develop business insights and strategic recommendations for brand reputation management.
- Conduct a scenario-based revenue projection to illustrate potential business implications for KFC.

## Dataset

| Information | Description |
|---|---|
| Data Source | YouTube Comments |
| Data Collection Period | October 17, 2023 – July 15, 2025 |
| Total Analyzed Comments | 6,102 |
| Number of Keywords | 8 |
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

The comments were collected from YouTube videos using the YouTube Data API, with up to 10 unique videos and a maximum of 250 comments per video for each keyword.

## Tools & Technologies

| Tool / Library | Purpose |
|---|---|
| Python | Data processing and analysis |
| Pandas | Data manipulation |
| NLTK | Tokenization and text processing |
| Sastrawi | Indonesian stemming |
| Emoji | Emoji removal |
| Scikit-learn | Bigram feature extraction using CountVectorizer |
| NetworkX | Bigram network analysis |
| WordCloud | Text visualization |
| Matplotlib & Seaborn | Data visualization |
| BERTopic | Topic modeling |
| UMAP | Dimensionality reduction |
| HDBSCAN | Clustering |

## Methodology

### 1. Data Collection

- Collected YouTube comments using the YouTube Data API.
- Used eight boycott-related keywords to identify relevant videos and discussions.
- Retrieved comments from different videos to capture diverse public perspectives.
- Combined the collected datasets and removed duplicate comments.

### 2. Data Preprocessing

Performed data preparation to ensure consistency and improve text quality.

The preprocessing steps included:

- **Sentiment Labeling:** Manually assigned sentiment labels to comments:
  - Positive (1): Supporting the use of boycotted products.
  - Neutral (2): Expressing neutral opinions, questions, or discussions.
  - Negative (3): Not supporting the use of boycotted products.
- **Data Filtering:** Removed non-Indonesian comments and comments identified as online gambling-related content.
- **Data Cleaning:** Removed URLs, mentions, hashtags, emojis, numbers, punctuation, and unnecessary spaces.
- **Text Normalization:** Converted informal words and slang into standardized Indonesian using a custom slang dictionary.
- **Stopword Removal:** Removed common and irrelevant words using Indonesian stopword lists and additional custom stopwords.
- **Stemming:** Converted words into their root forms using Sastrawi.
- **Tokenization:** Split processed comments into individual tokens for further text analysis.

The final dataset consisted of 6,102 comments after data cleaning and preprocessing.

### 3. Exploratory Data Analysis (EDA)

Conducted exploratory analysis to identify patterns and trends in public discussions.

The analysis included:

- Sentiment distribution across boycott-related keywords.
- Most popular keywords based on comment volume.
- Monthly trends in comment activity.
- Number of negative comments for each keyword.
- Duration of discussions associated with each keyword.
- Monthly sentiment trends for individual keywords.

### 4. Sentiment and Text Analysis

Analyzed the characteristics of positive, neutral, and negative comments through several text analysis techniques.

**Word Frequency Analysis**

Identified frequently occurring words to understand the main terms and themes discussed by netizens.

**WordCloud Visualization**

Visualized frequently occurring words separately for positive, neutral, and negative sentiment groups.

**Bigram Network Analysis**

- Extracted word pairs using CountVectorizer with a bigram range.
- Constructed word relationship networks using NetworkX.
- Applied degree centrality to identify words with the highest network connectivity.
- Examined relationships between frequently co-occurring words in each sentiment group.

**Additional Neutral Sentiment Analysis**

Since the initial word network for neutral comments was difficult to interpret, further analysis was conducted by:

- Identifying the 20 most frequent words in neutral comments.
- Examining neutral comment distributions across YouTube videos.
- Calculating the proportion of neutral comments for individual videos.
- Identifying videos with the highest proportion of neutral discussions.

### 5. Topic Modeling Using BERTopic

Applied BERTopic separately to positive, negative, and neutral sentiment groups to identify recurring discussion themes.

The modeling process incorporated:

- **BERTopic:** Extracting and grouping discussion topics.
- **UMAP:** Reducing text embedding dimensions.
- **HDBSCAN:** Clustering similar comments.
- **Topic Representation:** Identifying representative keywords and interpreting the resulting topics.

The analysis produced the following findings:

**Positive Sentiment – 29 Topics**

The three main discussion themes included:

1. **Product and Consumer Defense:** Discussions rejecting boycott campaigns and arguing that local consumers and businesses should not be blamed.
2. **Professionalism and Individual Choices:** Opinions that purchasing decisions are personal and should not necessarily be associated with political positions.
3. **Concerns for Local Businesses:** Discussions about the potential economic consequences of boycotts for local workers and UMKM.

**Negative Sentiment**

The main discussion themes included:

1. **Boycott Campaigns and Consumer Criticism:** Calls to boycott specific brands and criticism of consumers who continue purchasing their products.
2. **Local Economic Concerns:** Discussions about the potential consequences of boycotts for UMKM and local workers.
3. **Product Prices and Economic Nationalism:** Discussions encouraging consumers to choose local products and avoid expensive products associated with boycotted brands.

**Neutral Sentiment – More Than 52 Topics**

Neutral comments produced a wider variety of discussion topics, reflecting questions, opinions, and conversations that were not always directly related to the video context.

The topics included discussions about brands, consumer choices, Israel-Palestine issues, local products, and broader social and political debates.

## Key Findings & Business Insights

### 1. Neutral and Negative Sentiment Dominated Public Discussions

The final dataset showed the following sentiment distribution:

| Sentiment | Number of Comments | Percentage |
|---|---:|---:|
| Positive | 1,452 | 23.8% |
| Neutral | 2,653 | 43.5% |
| Negative | 1,997 | 32.7% |
| **Total** | **6,102** | **100%** |

Neutral and negative comments accounted for approximately 76.2% of the analyzed discussions, indicating substantial public attention toward boycott-related issues.

### 2. Boycott Campaigns Encouraged Interest in Local Products

Discussions highlighted local products and UMKM as alternatives to brands associated with boycott campaigns.

This suggests that boycott campaigns can encourage consumers to consider domestic products and support local businesses.

### 3. Neutral Consumers Focused on Price and Product Alternatives

Neutral discussions frequently revolved around product prices, quality, and alternative purchasing options rather than directly supporting or opposing boycott campaigns.

This suggests an opportunity for brands to attract consumers through competitive pricing, product quality, and value propositions.

### 4. Economic Concerns Emerged Across Different Sentiment Groups

Topic modeling revealed discussions about the potential impact of boycotts on local workers, employees, and UMKM.

Interestingly, concerns about local economic consequences appeared in both positive and negative sentiment groups.

### 5. Public Discussion Activity Increased During Certain Periods

Several boycott-related keywords experienced noticeable increases in discussion activity during November and December 2023.

Keywords such as #boikotunilever and #boikotstarbuck showed recurring increases in negative sentiment, while #produkisrael, #boikotkfc, and #boikotprodukisrael also experienced increases in neutral discussions.

### 6. Boycott Discussions Reflected Different Consumer Perspectives

The analysis identified different perspectives regarding consumer decisions, brand affiliations, humanitarian concerns, economic consequences, and support for local businesses.

The findings also suggest that some participants may have joined boycott discussions because of viral trends, although FOMO itself was not measured as a separate variable.

## Scenario-Based Revenue Projection: KFC

A scenario-based revenue projection was included in the final presentation to illustrate the potential financial implications of different customer retention and recovery strategies for KFC following boycott campaigns.

Unlike the main sentiment analysis, this simulation used a separate dataset consisting of **5,294 comments** related to the following keywords:

- #boikotkfc
- #aksiboikot
- #boikotprodukisrael
- #dampakboikot
- #penggantiprodukisrael
- #produkisrael

### 1. Sentiment Distribution

| Sentiment | Number of Comments |
|---|---:|
| Positive | 1,340 |
| Neutral | 2,391 |
| Negative | 1,563 |
| **Total** | **5,294** |

### 2. Simulation Assumptions

The projection used the following assumptions:

| Sentiment Group | Assumption |
|---|---|
| Positive | 100% assumed to remain loyal and continue purchasing |
| Neutral | 10%, 15%, or 20% assumed to potentially return as customers |
| Negative | 5% assumed to potentially return as customers |
| Average Transaction Value | IDR 50,000 per customer per day |

Three customer recovery scenarios were considered based on different conversion assumptions for neutral sentiment groups.

### 3. Calculation Framework

The estimated customer base for each scenario was calculated using:

**Estimated Customer Base = Positive Comments + (Neutral Comments × Conversion Rate) + (Negative Comments × 5%)**

The estimated daily revenue was calculated as:

**Estimated Daily Revenue = Estimated Customer Base × IDR 50,000**

### 4. Illustrative Scenario Results

The following figures are calculated from the assumptions and sentiment counts presented in the PPT.

| Component | Conservative (10%) | Moderate (15%) | Optimistic (20%) |
|---|---:|---:|---:|
| Retained Positive | 1,340 | 1,340 | 1,340 |
| Converted Neutral | 239.10 | 358.65 | 478.20 |
| Recovered Negative | 78.15 | 78.15 | 78.15 |
| Estimated Customer Base | 1,657.25 | 1,776.80 | 1,896.35 |
| **Estimated Daily Revenue** | **IDR 82.86M** | **IDR 88.84M** | **IDR 94.82M** |

### 5. Business Interpretation

The simulation illustrates how different customer recovery assumptions may influence potential revenue.

The optimistic scenario, which assumes a 20% conversion rate among neutral comments, produces the highest estimated daily revenue.

These scenarios highlight the potential importance of strategies targeting neutral consumers through competitive pricing, promotional campaigns, and improved brand communication.

**Simulation Limitations:**

This projection is an illustrative scenario based on hypothetical assumptions, not an actual sales forecast or measured business performance.

Social media comments do not necessarily represent unique customers or verified purchasing behavior. Therefore, the estimated customer base and revenue should be interpreted as hypothetical equivalents rather than actual customers and realized revenue.

The projection also represents potential gross revenue, not net profit, because operational expenses and cost of goods sold are not included.

## Business Recommendations

Based on the findings, the following strategies were proposed:

### 1. Build Trust Among Neutral and Negative Groups

Develop empathetic and informative communication strategies to address public concerns, improve brand perception, and rebuild consumer confidence.

### 2. Strengthen Brand Communication

Engage actively in public discussions through social media to respond to issues and communicate the values represented by the brand.

### 3. Clarify the Brand's Position

Communicate the brand's position regarding humanitarian issues transparently and consistently to reduce public misunderstandings.

### 4. Improve Product Quality and Price Competitiveness

Review product quality, pricing, and overall value propositions to remain competitive with local alternatives.

### 5. Implement Promotional and Soft-Selling Strategies

Introduce competitive promotions, discounts, and product bundles to attract price-conscious consumers without directly emphasizing controversial issues.

### 6. Establish Partnerships with Local Businesses

Collaborate with UMKM to strengthen relationships with local communities and demonstrate the brand's contribution to the domestic economy.

### 7. Highlight Positive Social Impact

Communicate the positive economic and social impacts generated through brand–UMKM collaborations.

### 8. Utilize Viral Moments for Brand Recovery

Take advantage of periods when public attention begins to decline to introduce relevant communication strategies and gradually rebuild brand reputation.

### 9. Monitor Public Sentiment and Emerging Issues

Continuously monitor social media discussions to identify potential reputational risks and develop appropriate responses.

## Project Conclusion

This project demonstrates how social media analytics and text mining can be used to understand public perceptions during consumer boycott campaigns.

The analysis identified a predominance of neutral and negative discussions, with recurring themes related to brand affiliations, humanitarian concerns, consumer purchasing decisions, local product alternatives, and the potential economic consequences of boycotts.

By combining sentiment analysis, exploratory data analysis, bigram network analysis, and topic modeling, the project translates unstructured YouTube comments into meaningful business insights.

The additional KFC revenue projection provides an illustrative business scenario to explore how customer retention and recovery assumptions may relate to potential revenue.

Overall, the project demonstrates the application of data analytics in supporting brand reputation management and business decision-making.

## Project Information

| Information | Description |
|---|---|
| Project Type | Collaborative Capstone Project |
| Project Domain | Social Media Analytics |
| Main Techniques | Sentiment Analysis, EDA, Text Mining, Topic Modeling |
| Data Source | YouTube |
| Programming Language | Python |
| Project Period | 2025 |

**Team Members**

- Uswatun Hasanah
- Syafiqah Marsya Kholiyadi
- Awalia Damayanti

**Project Contribution**

Data collection, sentiment labeling, data preprocessing, exploratory data analysis, visualization, insight development, presentation preparation, and project presentation.


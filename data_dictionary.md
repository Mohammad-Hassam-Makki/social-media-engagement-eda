# Data Dictionary

| Column | Type | Meaning | Cleaning |
|---|---|---|---|
| post_id | Text | Unique post ID. One row represents one post. | 60 exact duplicate rows removed |
| timestamp | Datetime | Date and time when the post was published (2023-01 to 2024-12). | Converted from text |
| platform | Category | Social media platform: Twitter, Instagram, Facebook, TikTok, LinkedIn. | Casing standardized |
| user | Text | Anonymized username. | None |
| followers_count | Numeric | Number of followers of the account. | Commas removed; 88 missing values kept as NaN |
| verified | Category | Account verification status: Yes, No, Unknown. | Missing values labeled Unknown |
| text | Text | Content of the social media post. | None; text appears templated |
| hashtags | Text | Hashtags used in the post. | Blank values represent no hashtags |
| country | Category | Country of the poster. | Casing standardized; missing values labeled Unknown |
| likes | Numeric | Number of likes received by the post. | 8 invalid negative values set to NaN |
| retweets_shares | Numeric | Number of shares or retweets received. | None |
| comments | Numeric | Number of comments received by the post. | 44 missing values kept as NaN |
| sentiment | Category | Sentiment classification: Positive, Neutral, Negative, Unknown. | Missing values labeled Unknown |
| hashtag_count | Integer | Number of hashtags used in a post. | Derived from hashtags |
| day_of_week | Category | Day of the week when the post was published. | Derived from timestamp |
| month | Integer/Category | Month when the post was published. | Derived from timestamp |
| total_engagement | Numeric | Combined engagement from likes, shares/retweets, and comments. | Derived in notebook |
| likes_per_1k_followers | Numeric | Likes normalized per 1,000 followers. | Derived in notebook; calculated using followers_count |

**Notes:**
- Each row represents one social media post.
- NaN represents missing or invalid numerical values.
- Derived features were created during data preprocessing and feature engineering.
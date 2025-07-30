## 📚 Table of Contents
1. [📚 Overview](#-overview)
2. [👥 Team Members & Contributions](#-team-members--contributions)
3. [📁 Files & Structure](#-files--structure)
4. [🌐 Data Sources & Acquisition](#-data-sources--acquisition)
5. [📊 Column Descriptions & Summary Statistics](#-column-descriptions--summary-statistics)
6. [🧪 Data Preprocessing & Analysis](#-data-preprocessing--analysis)
7. [🔍 Key Findings](#-key-findings)
8. [💻 Usage Instructions](#-usage-instructions)
9. [⚠️ Challenges & Limitations](#️-challenges--limitations)
10. [🚀 Potential Extensions](#-potential-extensions)
11. [📊 Data Distribution Plan](#-data-distribution-plan)

---# 📊 YouTube Trending Videos Analysis - DSCI-511 Final Project

## 📚 Overview
This project analyzes **YouTube** trends in 2024-2025 by programmatically collecting metadata from the **RapidAPI YouTube** endpoint, storing it in CSV format, and then analyzing content engagement patterns to derive strategic insights for content creators.

The dataset captures metadata from 2,155 trending videos across multiple regions (US, GB, AU) and content categories (music, gaming, movies), representing a combined viewership of 6.5 billion. It serves as a valuable resource for understanding content performance, audience engagement patterns, and optimal publishing strategies on one of the world's largest video platforms.

## 👥 Team Members & Contributions

1. **Amirreza Dast Parvardeh**
   - *Skills:* Machine Learning, Python, Full-Stack Web Development
   - *Contributions:* Assisted in data management and collection, developed advanced analytics for trend identification.

2. **Mubeen Yaqub**
   - *Skills:* Web Scraping, Automation, Python Programming
   - *Contributions:* Developed the primary data collection scripts (`main.py`), configured API integration, and implemented data extraction pipelines.

3. **Minahil Haroon Khalid**
   - *Skills:* Data Processing, Documentation
   - *Contributions:* Managed data consolidation, handled documentation, and prepared the final presentation with visualization support.

---

## 📁 Files & Structure
```
DSCI-511 Final Project/
├── Data.csv                 # Main cleaned dataset (2,155 trending videos)
├── Final.ipynb              # Jupyter Notebook with data collection code
└── analysis.ipynb           # Comprehensive data analysis and visualizations
```

### 🔍 Key Scripts

### 📊 Data Files
- **`Data.csv`**: Cleaned and processed dataset containing 2,155 unique trending videos

### 📓 Notebooks
- **`Final.ipynb`**: Contains data collection code, API integration, and initial processing
- **`analysis.ipynb`**: Comprehensive analysis with statistical breakdowns and visualizations

---

## 🌐 Data Sources & Acquisition
- **Primary Source:** RapidAPI's YouTube API integration providing trending video metadata
- **API Parameters:** Used geo and type filters to collect diverse content (US, GB, AU regions; music, gaming, movie categories)
- **Collection Strategy:** Implemented rate limit management (300 requests/day) through optimized query parameters and scheduled data collection
- **Data Elements:** Captured key metrics including video type, channel information, titles, view counts, publication dates, and duration

## 📊 Column Descriptions & Summary Statistics

| Column Name | Description | Sample Values | Data Type |
|-------------|-------------|--------------|-----------|
| `Type` | Content type classification | "video", "short" | String |
| `Channel Name` | Name of the content creator/channel | "Lady Gaga", "JENNIE", "Prime Video" | String |
| `Title` | Title of the trending video | "SIDEMEN CHARITY MATCH 2025", "Fix Your Pesky Back Foot" | String |
| `Channel ID` | Unique YouTube channel identifier | "UCDogdKl7t7NHzQ95aEwkdMw", "UCo4WuB8ozP-Qvx2FQLi5pIQ" | String |
| `Views` | Number of video views | 10745022, 36925, 597 | Integer |
| `Publication Date` | Date when video was published | "2025-02-12", "2025-03-08" | Date String |
| `Duration` | Video length in seconds | 0, 708, 1166, 1324 | Integer |

### 📈 Key Dataset Statistics
- **Total Records:** 2,155 unique trending videos
- **Total Views:** 6.5 billion combined views
- **Average Views:** 3.57 million per video
- **Median Views:** 698,119 views
- **Collection Period:** February-March 2025 (3 weeks)
- **Most Common Content Type:** Standard videos (vs. Shorts)
- **Most Viewed Video:** 96.1 million views
- **Average Duration:** 3:36 minutes (216 seconds)
- **Top Content Creator:** Lady Gaga (35 trending videos)
- **Popular Keywords:** "official" (501), "video" (353), "trailer" (291)

---

## 🧪 Data Preprocessing & Analysis

### 🧹 Data Cleaning & Normalization
1. **Standardization of View Counts**
   - Converted various notations (e.g., "4.2K", "1.2M") to integer values
   - Replaced missing values with zeros
   - Handled outliers through validation checks

2. **Date Formatting**
   - Normalized all publication dates to YYYY-MM-DD format
   - Derived day of week for temporal pattern analysis
   - Calculated recency metrics for trending analysis

3. **Duration Processing**
   - Converted duration strings (e.g., "9:55") to seconds for quantitative analysis
   - Created duration categories (e.g., "< 1 min", "1-3 mins") for grouping
   - Handled inconsistent formats and missing values

4. **Content Categorization**
   - Implemented keyword-based classification for content types
   - Applied natural language processing to extract themes from titles
   - Developed a taxonomy of video categories based on title analysis

### 📊 Analytical Techniques
- **Exploratory Data Analysis (EDA)**: Statistical examination of distributions and relationships
- **Temporal Analysis**: Patterns by day of week, time of day, and publishing recency
- **Content Analysis**: Title word frequency, theme extraction, and category performance
- **Channel Performance**: Analysis of top creators and their content strategies
- **Correlation Analysis**: Relationships between video attributes and performance metrics
- **Visualization**: Creation of interpretive charts, heatmaps, and statistical plots

---

## 🔍 Key Findings

### 👤 Content Creator Insights
- **Top Channels**: Lady Gaga leads with 35 trending videos, followed by Trending Shorts (30) and JENNIE (23)
- **Platform Diversity**: Music artists dominate with 5 of top 10 channels being music performers
- **Brand Presence**: Entertainment companies like Prime Video (16 videos) show strong performance
- **Content Focus**: HYBE LABELS and similar music production companies demonstrate significant trending potential

### 📅 Publishing Strategy
- **Optimal Day**: Thursday is the most effective publishing day with 404 trending videos (22% of all trending content)
- **Weekday Advantage**: Midweek content (Tuesday-Thursday) captures 57% of trending opportunities
- **Weekend Deficit**: Weekend content shows 57% lower trending potential than weekday content
- **Publishing Patterns**: Content published on Wednesday/Thursday averages 19% higher view counts

### ⏱️ Video Duration Performance
- **Optimal Length**: Short-form content (1-3 minutes) achieves highest engagement metrics
- **Duration Correlation**: Slight negative correlation (-0.19) between duration and views
- **Length Distribution**: 72% of trending videos fall under 5 minutes in length
- **Category-Specific Durations**: Each content category has an optimal duration range (e.g., gaming videos under 5 minutes outperform longer gaming content by 42%)

### 🎭 Content Categories
- **Dominant Types**: Music content leads trending videos with 27% higher average views
- **Title Keywords**: Popular terms include "official" (501 occurrences), "video" (353), and "trailer" (291)
- **Gaming Performance**: Gaming content (especially Minecraft, Fortnite, Roblox) shows strong engagement
- **Entertainment Previews**: Movie and TV trailers form a significant portion of trending content

---

## 💻 Usage Instructions

### 🔧 Required Software & Environment
- **Python 3.7+** with the following packages:
  - pandas (data manipulation)
  - numpy (numerical operations)
  - matplotlib & seaborn (visualization)
  - requests (API connectivity)
  - jupyter (notebook environment)
  - wordcloud (text visualization)

### 🔄 Understanding Our Workflow
Our project involves two main components that are contained in separate notebooks:

#### 1. Data Collection (Final.ipynb)
This notebook demonstrates the complete pipeline for collecting YouTube trending data:
- **API Configuration**: Shows how we connected to the RapidAPI YouTube endpoint
- **Data Extraction**: Documents our approach to retrieving trending video metadata
- **JSON Processing**: Explains how we parsed API responses and transformed them
- **Rate Limiting**: Demonstrates our solution for handling the 300 requests/day limit
- **Initial Cleaning**: Shows preliminary data transformations before storage

To understand our data acquisition process:
- Open `Final.ipynb` in Jupyter Notebook
- Review the cell-by-cell explanation of the collection methodology
- Observe how we implemented incremental data gathering across multiple days

#### 2. Data Analysis (analysis.ipynb)
This notebook contains our comprehensive analysis workflow:
- **Data Loading & Cleaning**: Detailed preparation of the dataset
- **Exploratory Analysis**: Statistical examination of trending patterns
- **Visualization Creation**: Generation of all charts and visual elements
- **Finding Extraction**: Systematic identification of key insights
- **Content Categorization**: Classification of videos by content type

To explore our analysis:
- Open `analysis.ipynb` in Jupyter Notebook
- Execute cells in sequence to reproduce our entire analytical process
- All visualizations will be generated as you progress through the notebook

All code is extensively commented to facilitate understanding and potential reuse.

---

## ⚠️ Challenges & Limitations

### 🔄 Data Collection Challenges
1. **API Rate Limitations**
   - RapidAPI's YouTube endpoint strictly limited us to approximately 300 requests per day
   - This constraint significantly reduced our ability to collect historical data
   - **Mitigation Strategy**: We implemented a distributed collection approach using multiple filter combinations and regions to maximize data diversity within limits

2. **Data Consistency Issues**
   - Inconsistent format of numerical values (e.g., "4.2K" vs "4200") required extensive normalization
   - Variation in date formats across different API responses necessitated standardization
   - **Mitigation Strategy**: Developed robust cleaning functions that handled multiple notation formats

3. **Missing Metadata**
   - Approximately 12% of video records had missing duration information
   - Some channel IDs were occasionally absent in API responses
   - **Mitigation Strategy**: Implemented fallback handling and annotation for missing values rather than discarding entries

### 📉 Analytical Limitations
1. **Temporal Constraints**
   - Our dataset spans only a 3-week period, limiting longitudinal trend analysis
   - Seasonal trends may not be fully captured in this snapshot
   - **Limitation Impact**: Findings may not generalize across different periods of the year

2. **Sampling Bias**
   - YouTube's trending algorithm has inherent biases that affect what content appears
   - Our results reflect YouTube's curation rather than pure viewer preferences
   - **Limitation Impact**: Insights are specific to content that YouTube promotes as trending

3. **Correlation vs. Causation**
   - While we identified correlations (e.g., video length and views), we cannot establish causation
   - Multiple confounding variables exist (e.g., creator popularity, production quality)
   - **Limitation Impact**: Recommendations based on findings should acknowledge this distinction

4. **Geographical Restrictions**
   - Primary focus on US, UK, and Australia limits global generalizability
   - Regional content preferences vary significantly across markets
   - **Limitation Impact**: Findings may not apply to other regional markets, particularly non-English speaking territories

### 💻 Technical Challenges
1. **Memory Management**
   - Processing the full dataset with multiple transformations required careful memory handling
   - Generating comprehensive visualizations occasionally triggered performance issues
   - **Mitigation Strategy**: Implemented incremental processing and optimized data types

2. **Collaboration Coordination**
   - Version control of notebooks between team members required structured communication
   - Merging independent analyses created occasional conflicts
   - **Mitigation Strategy**: Established clear division of analytical responsibilities and regular synchronization points

---

## 📊 Data Distribution Plan

### 📂 Dataset Accessibility
Our curated YouTube trending dataset is designed for academic and educational purposes with the following distribution approach:

1. **Current Distribution**
   - Included as `Data.csv` in this project submission
   - Full documentation of collection methodology and limitations provided
   - All data is publicly sourced from the YouTube API and contains no personally identifiable information

2. **Potential Future Distribution**
   - The dataset could be published on academic repositories for wider research access
   - A cleaned version could be shared on platforms like Kaggle for data science community use
   - Longitudinal extensions of this dataset would enhance its research value

### 📋 Usage Guidelines
We provide the following guidelines for ethical and effective use of this dataset:

1. **Educational Use**
   - Primary intended purpose is for educational analysis and content research
   - The dataset provides a valuable resource for teaching data science techniques

2. **Content Creator Insights**
   - Content creators can use the findings to inform publishing strategies
   - Analytics teams can benchmark performance against trending content metrics

3. **Ethical Considerations**
   - All data represents public information about trending videos
   - No private user data or engagement metrics beyond public view counts are included
   - Usage should comply with YouTube's terms of service

4. **Citation Requirements**
   - Academic or commercial use should cite this project and team members
   - Derivative works should acknowledge the original data source and collection methodology

### 🔄 Data Maintenance Considerations
For those continuing this research, we recommend:

1. **Regular Updates**
   - The trending landscape evolves rapidly, requiring periodic data refreshes
   - Our code infrastructure supports scheduled collection for longitudinal expansion

2. **Format Preservation**
   - Maintain consistent column naming and data formats for compatibility
   - Preserve temporal information to enable time-series analysis

---

*Submitted by:*
- **Mubeen Yaqub** - Web Scraping, Automation, Python Programming
- **Amir Dast Parvardeh** - Machine Learning, Data Analytics, Full-Stack Development
- **Minahil Haroon Khalid** - Documentation, Data Processing, Presentation

*March 16, 2025*

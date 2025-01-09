# Sentiment Analysis on Theme Park Reviews

The competition involved analyzing unstructured text. Performed sentiment analysis on 30,000+ customer reviews of Wisneyland Hong Kong to identify complaints and suggest improvements.
This project applies sentiment analysis techniques to a theme park reviews to derive insights into customer experiences. 
The analysis utilizes tools like Vader Sentiment Analyzer and generates visualizations to highlight trends in review sentiments.
This was for a school competition. 

## Project Overview

- **Goal**: Analyze customer reviews to extract sentiment scores (positive, negative, neutral, and compound) and visualize key insights.Then provide low-hanging fruit solutions and improvements for the theme park
- **Dataset**: A collection of theme park reviews, downloaded from an online CSV file.
- **Key Tools**: Python libraries including Pandas, NLTK, Matplotlib, Seaborn, and WordCloud.

## Features

1. **Sentiment Scoring**:
   - Uses NLTK's Vader SentimentIntensityAnalyzer to assign sentiment scores to each review.
   - Extracts compound, positive, neutral, and negative sentiment metrics.

2. **Data Visualization**:
   - Generates visualizations to show sentiment trends.
   - Includes word clouds to highlight common themes in reviews.

3. **Export Functionality**:
   - Saves the processed data with sentiment scores to a CSV file for further use.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/MSBA-Analytics-Challenge.git
   cd theme-park-sentiment-analysis
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Run the notebook:
   - Open `NLP_challenge_code.ipynb` in Jupyter Notebook or a similar IDE.
   - Execute cells sequentially to perform data loading, analysis, and visualization.

2. Download the processed data:
   - The analysis saves the results as `review_scores.csv` in the working directory.

## Results

- Extracted sentiment scores for each review.
- Created compound sentiment scores for overall positivity or negativity trends.
- Visualized key themes in the dataset using word clouds and sentiment distribution graphs.

## Dependencies

- Python 3.7+
- Pandas
- Matplotlib
- Seaborn
- NLTK
- WordCloud

## Contributions

Feel free to open issues or submit pull requests if you would like to contribute to this project.

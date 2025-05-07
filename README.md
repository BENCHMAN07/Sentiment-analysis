# Sentiment-analysis
Sentiment Analysis Instagram using a Benchmark Dataset from Github

Here's a sample **README** file for your project, explaining the implementation of the Instagram CSV part:

---

# Social Media Sentiment Analysis Dashboard

This project provides a web-based dashboard to analyze sentiment and user satisfaction for Instagram posts and comments. The project uses **Flask**, **Pandas**, and **TextBlob** to analyze and categorize user comments based on sentiment, likes, and replies.

## Project Overview

The dashboard includes two main sections:

1. **Instagram QoS Dashboard**: This section analyzes Instagram comments and displays average sentiment and user satisfaction statistics.
2. **Twitter QoS Dashboard**: This section (yet to be implemented for Twitter dataset) will display similar metrics for Twitter comments.

### Technologies Used:

* **Flask**: Web framework for Python to build the application.
* **Pandas**: Data manipulation and analysis.
* **TextBlob**: Sentiment analysis tool.

---

## Project Structure

The project is organized in the following folder structure:

```
/social_media_sentiment_analysis
│
├── /app.py                # Main Flask application file
├── /analysis.py           # Sentiment analysis and satisfaction classification logic
├── /templates/
│   ├── dashboard.html     # Instagram dashboard HTML template
│   └── twitter_dashboard.html  # Twitter dashboard HTML template
├── /static/
│   └── style.css          # Custom CSS for dashboard styling
└── /data/
    └── Instagram-datasets.csv  # Instagram dataset for analysis
```

---

## Requirements

To run the project, you will need the following libraries installed:

* **Flask**: `pip install flask`
* **Pandas**: `pip install pandas`
* **TextBlob**: `pip install textblob`

---

## Setup

1. Clone or download the project files.

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Make sure you have the following dataset:

   * `Instagram-datasets.csv`: This file contains Instagram comments data and is located in the `data/` directory.

   **Instagram Dataset Structure**:

   * **comment**: The comment text.
   * **likes\_number**: The number of likes on the comment.
   * **replies\_number**: The number of replies to the comment.
   * **comment\_user**: Username of the user who made the comment.
   * **comment\_date**: Date when the comment was posted.

---

## Running the Application

1. Open a terminal and navigate to the project directory.

2. Run the Flask application:

   ```bash
   python app.py
   ```

3. Open your browser and go to:

   ```
   http://localhost:5000/
   ```

   This will display the **Instagram QoS Dashboard**, which shows:

   * **Average Sentiment**: An average sentiment score of all Instagram comments.
   * **Satisfaction Statistics**: A breakdown of comments classified as 'Positive', 'Neutral', or 'Negative' based on sentiment and engagement (likes and replies).

---

## Key Features

1. **Instagram Sentiment Analysis**:

   * The app reads the `Instagram-datasets.csv` file and performs sentiment analysis on the comments using **TextBlob**.
   * Sentiment is classified into categories such as 'Positive', 'Neutral', and 'Negative'.

2. **Satisfaction Classification**:

   * The app classifies comments based on the number of likes, replies, and sentiment. The classification is performed in the `classify_satisfaction` function.

3. **Dashboard Display**:

   * Displays a dashboard with visual insights, including:

     * Average sentiment score for all comments.
     * A count of comments in each satisfaction category.

---

## Instagram CSV Implementation

The core of the Instagram sentiment analysis starts by reading the dataset from the CSV file located at `data/Instagram-datasets.csv`. The script:

1. **Reads the CSV** using `pandas`.
2. **Renames Columns** to match the format used in the application (e.g., `comment` -> `Comment`, `likes_number` -> `Likes`).
3. **Drops rows with missing comments** to ensure the analysis is accurate.
4. **Applies Sentiment Analysis** on the `Comment` column using **TextBlob**.
5. **Classifies User Satisfaction** based on the sentiment score, likes, and replies.

---

## Sample Instagram CSV Format

The `Instagram-datasets.csv` file should have the following columns:

| comment                  | likes\_number | replies\_number | comment\_user | comment\_date | ... |
| ------------------------ | ------------- | --------------- | ------------- | ------------- | --- |
| "Great post!"            | 120           | 10              | user1         | 2025-05-01    | ... |
| "This is amazing!"       | 200           | 15              | user2         | 2025-05-02    | ... |
| "Not bad, could improve" | 50            | 5               | user3         | 2025-05-03    | ... |

---

## Next Steps

1. **Twitter QoS Dashboard**: Implement functionality for analyzing Twitter data using a similar structure.
2. **Visualizations**: Enhance the dashboard with graphs and charts for better visual representation.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

![image](https://github.com/user-attachments/assets/dcac852a-a75e-41e6-8a39-96101c0d2d6b)

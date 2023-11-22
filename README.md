# NIFTY50_Stock_Price_Prediction  
![Screenshot (392)](https://github.com/mdkamran048/NIFTY50_Stock_Price_Prediction/assets/143988392/8f9404db-b86e-47ca-82c6-b05277f21738)


This project focuses on stock price prediction for NIFTY-50 stocks using a robust model trained on four years of historical data. 
Users can input their stock preferences, quantities, buying and selling dates, allowing for portfolio analysis. 
Whether predicting future prices or using historical data, the model calculates the portfolio's returns, streamlining the process through integration with Google Sheets. 
This project provides a powerful tool for investors to make informed decisions and analyze their investments effectively.

## Folder Structure
| Files | Description |
|-------| ------------|
| **NIFTY50_Stocks_Data** | This folder includes raw datasets, as well as the merged data used for model creation and analysis. |
| **NIFTY50_Stocks_Gsheet** | This folder houses all files related to Google Sheets integration, including the model and datasets. |
| **NIFTY50_Web-Scraping** |  "Web_Scraping" folder comprises an IPython Notebook (IPYNB) file for web scraping purposes. |
| **README.md** | "README.md" serves as the project's informational documentation. |

## Introduction  
- As an investment advisor the aim of this project was to predict future prices of Nifty50 stocks using advanced machine learning algorithms
- Here the Investors can use our model to make well-informed decisions based on data-driven insights.
- The platform allows users to enter stock details and receive approximate profit/loss estimations
- Our model will empowers investors to optimize their portfolios and enhance trading strategies with reliable forecasts.

## Objectives

**Objectives:**  
* Understand the Importance of Nifty50
* Describe Data Sources
* To Showcase Model Accuracy
* To Demonstrate Webpage Interface
* To predict profit/loss based on user’s:
	Stock name 
	Quantity 
	Buying date 
	Selling date
* Emphasize Real-world Applications
* Future Plans

**Problem Statement:**
- To develop a script to scrape NIFTY-50 stock data for the past 4 years.
- To train stock price prediction models for each NIFTY-50 stock.
- To develop logic for calculating returns using predicted or historical prices.
- To facilitate input and output in a Google Sheet for user convenience.
- To create an attractive front-end offering essential portfolio statistics.
- To provide users with a holistic tool for stock predictions and portfolio analysis.

## Importance of Nifty50
![Picture1](https://github.com/mdkamran048/NIFTY50_Stock_Price_Prediction/assets/143988392/a63ba5f3-e37d-4189-8663-5be58c4d13d0)

- Nifty50 is India's benchmark stock market index, representing the performance of the top 50 companies in the country
- It serves as a crucial indicator of the overall health and direction of the Indian economy.
- Nifty50 significantly influences investor sentiment, guiding investment decisions and portfolio strategies.
- The index reflects market trends, helping investors gauge the overall performance and direction of the stock market.

## Preprocessing

**Web Scraping:**  
- Data sourced exclusively from official and reputable websites, including "https://in.investing.com/".
- Four years of NIFTY50 stock information extracted meticulously to ensure dataset reliability and credibility.

**Null and Noise Handling:** 
- Thorough assessment conducted to identify and address null values in the dataset.
- Implemented noise reduction techniques to enhance data accuracy, ensuring a cleaner dataset.

**Unwavering Data Type Uniformity:**   
- Meticulous standardization of data types applied consistently across the entire dataset.
- Eliminated discrepancies and irregularities in data types, promoting seamless data processing and accurate analytical insights.

**Data Size and Structure Assessment:** 
- Comprehensive evaluation performed on the size and shape of each data table.
- Provides an insightful understanding of the dataset's intricate structure, laying the foundation for comprehensive data analysis.

**Strategic Data Compilation and Filtering:**  
- Aggregated and organized NIFTY-50 stock data by stock names for easy data filtration and retrieval.
- Enables precise selection and extraction of data relevant to users' preference of stock for predicting profit or loss based on specific buying and selling dates.

**Cleaned Data**  
![Screenshot (393)](https://github.com/mdkamran048/NIFTY50_Stock_Price_Prediction/assets/143988392/469761d2-8eca-428c-9a7f-8f1faf25b266)


By executing these preprocessing steps, the dataset was refined, cleaned, and made ready for further analysis, establishing a solid foundation for accurate prediction.

## Model Building
![Screenshot (394)](https://github.com/mdkamran048/NIFTY50_Stock_Price_Prediction/assets/143988392/7008ccd3-1210-49e3-a8a5-dd28e3b7565b)

- Our machine learning model utilizes polynomial regression to predict profit/loss in Nifty50 stocks.
- Accurate predictions assist investors in making informed decisions.
- The model is trained on historical stock data to ensure reliability.
- It offers a user-friendly interface for inputting stock details and obtaining predictions.
- This project showcases the application of Artificial Intelligence and Machine Learning in real-world financial analysis.

## Google Sheet Integration
<pre><code>
# Importing Dataset
all_data=pd.read_excel('D:/Data Analyst Course/Project_Nifty50/NIFTY50_Stocks_data.xlsx')

# Setting parameters
scope = ['https://spreadsheets.google.com/feeds', 'https://www.googleapis.com/auth/drive']
credentials = ServiceAccountCredentials.from_json_keyfile_name('chromatic-pride-392908-ccf371b70a0f.json', scope)
client = gspread.authorize(credentials)

sheet_key = '1-biUonUrbRltqeXIadCUyGpHItCDvljh4JuukYqEODk'
sheet = client.open_by_key(sheet_key)

worksheet = sheet.get_worksheet(0)
</code></pre>

![Screenshot (395)](https://github.com/mdkamran048/NIFTY50_Stock_Price_Prediction/assets/143988392/201b4698-fc9b-48cf-8f2a-db074baf8b87)


- Integrated our machine learning model directly into Google Sheets for effortless stock analysis.
- It allows users to input Stock name, quantity, buying  and selling dates.
- Our model will instantly calculates whether they would make a profit or incur a loss based on historical data and predictions.

## Model Application

- Informed Investment Decisions  
- Risk Management  
- Portfolio Optimization  
- Financial Planning  
- Enhancing Market Understanding  
- Empowering Individual Investors  
- Confidence in Decision-making  
- Validating Existing Strategies  
- Future Applications
  
![Screenshot (396)](https://github.com/mdkamran048/NIFTY50_Stock_Price_Prediction/assets/143988392/a86b1363-6631-4817-886e-c9e1b2c30358)


- Our model will leverages the power of data and machine learning to empower investors and traders with valuable insights, fostering data-driven decision-making and enhancing overall performance in the financial sector.

## Future Plan

* Fetching the live data and automate the model on the server.
* If it works fine then deploying over the server so that users can use it.

## Model Limitation  
**Limited data:**  
- Utilizing only 4 years of historical data might not capture long-term trends and patterns that could significantly influence stock prices.
  
**Overfitting risk:**  
- Polynomial regression may lead to overfitting due to its sensitivity and small fluctuations in the data.
  
**Limited input features:**  
- Relying solely on close price, volume, and date might not encompass all relevant factors impacting stock performance.
  
**Market complexity:**  
- The stock market is influenced by multifaceted factors, including geopolitical events, macroeconomic and microeconomic trends, which may not be accounted for in the model.

## Challenges
- Integrating the machine learning model with Google Cloud and Google Sheets posed initial challenges.
- Deploying the model on the web page required optimizing performance and ensuring functioning of the web page.
- Coordinating frontend and backend development for seamless user experience was a complex task.
- Overcoming hurdles in data handling and processing to deliver accurate predictions to users.

## Learning
**Web Scraping Mastery:**  
- Attained a high level of competence in web scraping techniques, enabling efficient and reliable data acquisition from online sources, notably exemplified by NIFTY50 stock price data extraction.

**Data Preprocessing Expertise:**  
- Cultivated strong skills in data cleaning and preprocessing, ensuring the data's integrity, consistency, and suitability for analysis and prediction. 

**Machine Learning Integration:**  
- Successfully integrated machine learning models with Google Sheets, showcasing the ability to bridge the gap between data analysis and real-world applications, particularly in the context of stock price prediction.

**Insightful Data Analysis:**  
- Acquired the capability to employ various analytical tools and methodologies to derive valuable insights from complex datasets, facilitating informed decision-making processes.

**Problem-Solving Aptitude:**  
- Applied data-driven insights and machine learning models to formulate pragmatic solutions to real-world challenges, exemplified by predicting NIFTY50 stock prices for future investment decisions.

**Interactive Webpage Creation:**  
- Developed proficiency in creating user-friendly web interfaces and interactive web pages, enhancing user engagement and facilitating data presentation in a user-friendly manner.

**Client Communication Skills:**  
- Strengthened the ability to effectively communicate with clients, addressing their queries, and tailoring data-driven solutions to meet their specific needs, thereby fostering strong client relationships.

**Project Management Competency:**  
- Demonstrated project management skills by effectively coordinating various tasks, from data acquisition and preprocessing to model integration and web development, ensuring project success and timeliness.

**Continuous Learning Mindset:**  
- Embraced a growth-oriented mindset, actively seeking out new techniques, tools, and technologies to stay at the forefront of data science and web development, thereby ensuring the project's ongoing relevance and effectiveness.

These learnings not only highlight our project's accomplishments but also underscore our growth and development as a data scientist and web developer, showcasing our ability to tackle complex challenges and deliver practical solutions.

## Conclusion  
* Our team successfully developed a Google sheet and also web-based machine learning model utilizing polynomial regression to predict profit/loss in Nifty50 stocks. 
* Users can input stock details, quantity, buying, and selling dates to get predictions for his/her portfolio either he/she will be in profit/loss. 
* This project demonstrates our collaborative efforts in applying AI for real-world financial analysis and decision-making.

|---------------------------------------------------------------------------------------------------------------------------|


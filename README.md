# Nasdaq-100 Stock Analysis Using the OpenAI API

## Project Overview

This project uses **Python, pandas, and the OpenAI API** to analyze the year-to-date (YTD) stock performance of Nasdaq-100 companies headquartered in California.

The goal is to combine traditional data analysis with generative AI to classify companies into market sectors, compare sector performance, and generate AI-powered stock recommendations based on historical performance.

This project was completed as part of a DataCamp Python and AI learning project.

## Technologies Used

- **Python** — Data processing and analysis
- **pandas** — DataFrames, merging datasets, grouping, and sorting
- **OpenAI API** — AI-powered company classification and stock analysis
- **Jupyter Notebook** — Development and execution
- **DataCamp DataLab** — Cloud-based development environment

## Dataset

The project uses two CSV files provided by DataCamp:

**1. `nasdaq100_CA.csv`**

Contains information about Nasdaq-100 companies headquartered in California, including company names, stock symbols, headquarters, and founding dates.

**2. `nasdaq100_price_change.csv`**

Contains stock performance data across different periods, including daily, monthly, yearly, and year-to-date changes.

Both datasets are merged using the stock ticker (`symbol`) as the common identifier.

## Project Workflow

### 1. Data Loading and Preparation

- Load CSV files using pandas.
- Merge company information with stock performance data.
- Create a DataFrame containing the YTD performance for each company.

### 2. AI-Powered Sector Classification

Use the OpenAI API to classify companies into sectors, including:

- Technology
- Communication
- Consumer Cyclical
- Healthcare
- Financial
- Industrials
- Energy
- Utilities
- Real Estate
- Consumer Defensive

A reusable Python function sends company names to the OpenAI API and extracts the returned sector classifications.

### 3. Sector Performance Analysis

- Group companies by their assigned sectors.
- Calculate average YTD performance using pandas.
- Rank sectors based on average performance.
- Identify the strongest-performing sectors in the dataset.

### 4. AI-Generated Stock Recommendations

Send the selected sector and company performance data to the OpenAI API to generate:

- Summaries of sector performance
- Company recommendations based on YTD performance
- Explanations of the selected companies' performance

The AI-generated output is stored in the `stock_recommendations` variable.

## Example Results

The following results are based on the historical dataset used in this project.

| Sector            | Average YTD Performance |
| ----------------- | ----------------------: |
| Communication     |                 +49.44% |
| Technology        |                 +48.62% |
| Consumer Cyclical |                 +18.00% |

These values reflect the dataset and are not live market figures. Sector classifications are AI-generated and may require validation.

## How to Run

1. Clone or download this repository.

2. Install the required Python packages:

   ```bash
   pip install pandas openai
   ```

3. Configure an OpenAI API key using the `OPENAI_API_KEY` environment variable.

4. Open `notebook.ipynb` in Jupyter Notebook or VS Code.

5. Run the cells in order to reproduce the analysis.

**Note:** OpenAI API access requires valid credentials. API requests may incur usage charges.

## Key Skills Demonstrated

- Working with external REST APIs through a Python SDK
- Creating reusable Python functions
- Prompt engineering for structured classification tasks
- Manipulating and merging datasets with pandas
- Performing group-based statistical analysis
- Integrating generative AI into a data analysis workflow
- Interpreting AI-generated responses

## Limitations

- Stock performance is based on a historical dataset rather than live prices.
- AI-generated sector classifications may occasionally be incorrect.
- Higher historical returns do not guarantee future performance.
- Recommendations are educational and should not be interpreted as personalized financial advice.

## Future Improvements

- Integrate live stock market data.
- Validate AI sector classifications against an established classification standard.
- Add data visualizations showing sector performance.
- Implement automated checks for AI response accuracy.
- Build an interactive dashboard using Streamlit.

## Acknowledgment

Project based on DataCamp's *Enriching Stock Market Data using the OpenAI API* exercise.

Dataset and original project instructions provided by DataCamp.

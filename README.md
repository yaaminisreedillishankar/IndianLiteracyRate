📘 Literacy & Population Data Scraping, Cleaning & Visualization (India)

This project scrapes, cleans, validates, and analyzes literacy rate and population-based literacy trends for India using data from Wikipedia and government-backed survey sources. It produces two structured datasets and several visual insights that help understand literacy growth patterns across states and union territories.

📝 Project Overview
Objective

To extract and clean two major literacy-related datasets from authoritative online tables, structure them in CSV format, and generate visualizations showing literacy improvements and demographic progress across India.

Datasets Extracted:
The project produces two datasets, aligned exactly to the structure of the source tables:

1. Literacy_Rate.csv

This dataset corresponds to the Wikipedia table “Literacy rates as %age of population aged seven and older” with the following column :

State/UT
Census 2011	Total, Male, Female
NSC Survey (2017)	Total, Male, Female
PLFS Report (2024)	Total, Male, Female

This dataset provides the latest official and survey-based literacy percentages across Indian states/UTs for three key years.

Use Cases:

Comparison of literacy by gender
Trend evaluation from 2011 → 2017 → 2024
State-level literacy ranking
Visualization and socio-economic analysis

2. Literacy_rate_population.csv

This dataset corresponds to the Wikipedia table:

“Census — Literacy rate as % of population” containing literacy percentages across seven Census years:

Column	Description
State/UT	Name of the state or union territory
1951	Literacy %
1961	Literacy %
1971	Literacy %
1981	Literacy %
1991	Literacy %
2001	Literacy %
2011	Literacy %

Average Population	Derived metric used in charts (optional)
About Average Population

This field is not from Wikipedia, but is computed from the dataset as:
A mean literacy percentage across the Census year (or a weighted average when population data is included in visualizations).

Technologies & Libraries

1. Python 3
2. requests — Fetching HTML pages
3. BeautifulSoup4 — Parsing HTML tables
4. pandas — Table extraction, cleaning, CSV export
5. matplotlib — Line charts, pie charts
6. folium — India literacy map
7. re — Cleanup operations

📂 Project Structure
project-folder/
│── MiniProject.ipynb                # Main scraping & analysis notebook
│── Literacy_Rate.csv                # Table: Literacy rates (Census 2011, NSC 2017, PLFS 2024)
│── Literacy_rate_population.csv     # Table: Census literacy rates (1951–2011)
└── README.md                        # Documentation

▶️ How to Run the Project

Install dependencies:

python3 -m pip install requests beautifulsoup4 pandas matplotlib folium

Open the notebook:
MiniProject.ipynb

Run all cells:

Both datasets will be generated/cleaned.
Visualizations (maps, charts) will be rendered.

Visual Outputs:

1. Literacy Trends Map (Folium)
Shows PLFS 2024 literacy % across Indian states geographically.

2. Line Chart — Census Literacy (1951–2011)
Displays the long-term improvement in literacy for each state.

3. Pie Chart — Average Literacy Measure
Uses the Average Population/Literacy metric to visualize state contribution.
Visual Outputs

4. Average Male vs Female Literacy Rate by Survey
Compares average literacy rates of males and females across 2011 Census, NSC 2017, and PLFS 2024.

5. Bottom 5 States/UTs Literacy Rate Comparison by Year
Lollipop chart showing the lowest 5 states/UTs by literacy rate for 2011, 2017, and 2024.

6. Top 10 States by Literacy Improvement (2011–2024)
Scatter plot identifying the ten states/UTs with the largest literacy improvement.

7. Literacy Gender Gap Trend (2011–2024)
Shows the trend of the average gender gap in literacy across the three surveys.

8. Total Literacy Rate by State/UT (2011, 2017, 2024)
Horizontal grouped bar chart of total literacy rates for each state.

9. Female Literacy Rate by State/UT (2011 vs 2017 vs 2024)
Horizontal bar chart showing female literacy rates across the three survey years.

10. Male Literacy Rate by State/UT (2011 vs 2017 vs 2024)
Horizontal bar chart showing male literacy rates across the three survey years.

11. Average Literacy Rate by Region (2011 vs 2017 vs 2024)
Bar chart showing average literacy across Indian regions for the three surveys.

12. Top 5 States/UTs Literacy Rate Comparison by Year
Horizontal bar charts showing the top 5 states/UTs for each survey year.

13. Overall Average Population by Decade (1951–2011)
Pie chart showing average population contribution by decade.

Limitations:

1. Some newer UTs (Ladakh, Telangana) do not have historical Census data.
2. Minor differences across Census, NSC, and PLFS methodologies.
3. Wikipedia table structure may change over time, requiring updates.

Future Enhancements:

1. Automated multi-year updating via GitHub Actions
2. Combined literacy + GDP + education spending dataset
3. Forecasting literacy using ML models
4. Interactive dashboard using Streamlit

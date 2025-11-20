**Current Status of Course Project Goals:**

**Data Lifecycle (Complete)**

The data within this project most closely relates to the USGS Science Data lifecycle discussed previously in class. The USGS lifecycle contains 6 linear steps (Plan, Acquire, Process, Analyze, Preserve and Publish) which each involve cross-cutting activities. The data lifecycle of this project involves each of these steps aside from the Preserve one, as this data will not be preserved in any highly stable location such as most science data would be (such as within a University library or catalogue). Each of these other steps has either already been performed within the scope of this project (Plan, Acquire and some of Process) while the rest will come as this project continues in its trajectory to completion.

**Ethical Data Handling (Complete)**

Unemployment Rate data was provided by the U.S. Bureau of Labor Statistics via the FRED API, falling into the Public Domain of free use. Each of these datasets does request the usage of a citation, which will be provided below.

U.S. Bureau of Labor Statistics, Unemployment Rate in Dallas County, TX [LAUCN481130000000003A], retrieved from FRED, Federal Reserve Bank of St. Louis; https://fred.stlouisfed.org/series/LAUCN481130000000003A, November 14, 2025.

U.S. Bureau of Labor Statistics, Unemployment Rate in Harris County, TX [LAUCN482010000000003A], retrieved from FRED, Federal Reserve Bank of St. Louis; https://fred.stlouisfed.org/series/LAUCN482010000000003A, November 14, 2025.

U.S. Bureau of Labor Statistics, Unemployment Rate in El Paso County, TX [LAUCN481410000000003A], retrieved from FRED, Federal Reserve Bank of St. Louis; https://fred.stlouisfed.org/series/LAUCN481410000000003A, November 14, 2025.

U.S. Bureau of Labor Statistics, Unemployment Rate in Austin County, TX [TXAUST5URN], retrieved from FRED, Federal Reserve Bank of St. Louis; https://fred.stlouisfed.org/series/TXAUST5URN, November 14, 2025.

Estimate Median Household Income data was provided by the U.S. Census Bureau also via the FRED API, which also falls into the Public Domain. These datasets also ask for a citation, which will be below.

U.S. Census Bureau, Estimate of Median Household Income for Dallas County, TX [MHITX48113A052NCEN], retrieved from FRED, Federal Reserve Bank of St. Louis; https://fred.stlouisfed.org/series/MHITX48113A052NCEN, November 14, 2025.

U.S. Census Bureau, Estimate of Median Household Income for Harris County, TX [MHITX48201A052NCEN], retrieved from FRED, Federal Reserve Bank of St. Louis; https://fred.stlouisfed.org/series/MHITX48201A052NCEN, November 14, 2025.

U.S. Census Bureau, Estimate of Median Household Income for Austin County, TX [MHITX48015A052NCEN], retrieved from FRED, Federal Reserve Bank of St. Louis; https://fred.stlouisfed.org/series/MHITX48015A052NCEN, November 14, 2025.

U.S. Census Bureau, Estimate of Median Household Income for El Paso County, TX [MHITX48141A052NCEN], retrieved from FRED, Federal Reserve Bank of St. Louis; https://fred.stlouisfed.org/series/MHITX48141A052NCEN, November 14, 2025.

As all of these datasets fall within the public domain of free use and are widely available on the internet, I have no reservations about the usage of this data for exploratory data analysis. There is no identifiable information about specific persons or groups within the dataset, and the people who provided this data already gave consent to the Federal Government to collect, analyze and report said data to the public.
The High Value dataset on the currently incarcerated inmate population within the state of Texas is the other dataset used for this project. It was provided by the Texas Department of Criminal Justice via the Texas Open Data Portal. While no specific license is listed for use of this dataset, it does fall within the umbrella of public domain as criminal information is always made available to the public.The usage of this data can vary depending on the State or Department it was retrieved from, but the Texas Open Data Portal functions as it is named, “to serve as the official repository for publicly accessible state data to increase transparency, accountability, and efficiency in government” (TODP). It allows complete retrieval, analysis and publication of the data on its page free of charge. While no specific attribution is requested for the use of this data, I will provide one below to remain transparent in my goal of ethical data handling.
Texas Department of Criminal Justice, High Value Dataset: August 2025, retrieved from TODP, Texas Open Data Portal; November 14, 2025. https://data.texas.gov/dataset/High-Value-Dataset-August-2025/9b32-yeu6/about_data
There is some personally identifiable information provided within the dataset that, during data cleaning, I will remove for the purposes of remaining as ethical as possible. These attributes include: SID Number, TDCJ Number, Name and Case Number. These pieces of information will not improve our analysis of this data and only serve to create potential data ethics issues when this data analysis is published again. While this data is openly accessible by any member of the public, I won’t allow my data analysis to be used for predatory or unethical purposes. 

**Data Collection & Acquisition (In Process)**

Each dataset related to the Unemployment Rate or Median Household Income for a specific Texas County will be pulled from the FRED API, a highly reliable data storage service for Federal Reserve Economic Data, via the requests library in Python. I have successfully pulled a couple of the datasets from the FRED API that were cited above and will be creating a function to help me pull the rest of these datasets in the next phase of development (See Python Workbook). The High Value Dataset was downloaded as a CSV directly from the TODP website which is a similarly highly reliable data curation website provided to the public by the Texas Government, and in the case of this specific dataset, by the Texas Department of Criminal Justice. The file is currently too large to upload directly to GitHub so I plan to take a subset of the original file (just the counties of interest to me) and then upload that as a csv to this repository.
I currently am only using the FRED API data for 2020-2024 but may change this to a larger subset of time data to allow for more analysis of time trends.

**Storage and Organization (In Process)**

The High Value Dataset on incarcerated individuals uses a CSV structure, which I will pull into Python directly. Once loaded, I’ll use the Pandas library to convert the data into a dataframe so I can perform analysis on it.
Using the requests library, I was able to use a pull request to obtain the FRED data from the API and then load it into a JSON file type. Similar to the CSV structure of the other dataset, I can use Pandas to turn the JSON file data into a Pandas dataframe, thus making sure each dataset has the same structure, allowing for easier and more effective analysis.

**Extraction and Enrichment (In Process)**

As I was able to obtain the data in a semi structured format directly from the FRED API and TODP websites, a minimal amount of data extraction will need to be conducted. The datasets will undoubtedly require cleaning, but no data extraction practices mentioned in class (such as NER or computer vision) will need to be used, as the relevant information is already available in the dataset.
As far as enrichment is concerned, as I will be combining all unemployment rate datasets together, as well as all median household income ones, I will enrich the data by adding a County identifier attribute so I can properly analyze differences amongst counties even once the data has been integrated.

**Data integration (Complete)**

As discussed previously, I was able to convert the FRED API data from its original structure from the requests library into a JSON structure, then into a Pandas dataframe. I was also able to turn the Texas Incarceration dataset into a Pandas dataframe from its original CSV format. By ensuring these datasets have the same format, analysis will be much more streamlined. I don’t believe I will fully integrate these datasets and put them into one large dataset, I believe keeping them as two separate datasets (one for crime information and the other for economic) will yield better analysis results.

**Data Quality (Planned)**

Planned to complete over Thanksgiving break.

**Data Cleaning (Planned)**

Planned to complete over Thanksgiving break.

**Workflow Automation and Provenance (Planned; May Need Additional Input)**

I may need some guidance on this, I can make functions to help streamline the process but the small amount of information we learned about workflow automation may not be enough for me to fully implement one for this project.

**Reproducibility and Transparency (Planned)**

Planned for between Thanksgiving break and the due date.

**Metadata and Data Documentation (Planned)**

This has been happening throughout the project process and I will put the finishing touches after Thanksgiving break.

**Changes Since Proposal**

Original Research Questions:
How does the unemployment rate of an area impact the crime rate for said area?
How does the median household income of an area impact the crime rate for the area?

New Research Questions: 
What kind of relationship exists, if any, between the unemployment rate and crime rate of an area?
What kind of relationship exists, if any, between the median household income and crime rate of an area?

I was advised to keep causative language out of my research questions, so I changed this to a more neutral term of “relationship”.

**Gaps**

I originally couldn’t think of any gaps in my proposed research but since we have learned more about workflows, I find myself unsure of whether I will be able to properly create and implement a workflow for my entire project. With the small amount of experience we gained through the Snakemake lab, I am not confident in my ability to translate this experience into a final product for this project on my own. I may need additional input for this section of the project.

# Covid-19 Testing, Infections, Death Rates

## Project Objective

In this project, an analysis was made on how USA has done in terms of Covid Testing and Controlling Covid Cases & Deaths compared to the Rest of the World. 

## Data Used

For this purpose, a Covid-19 dataset from the website <a href = "https://ourworldindata.org/covid-deaths"> Our World in Data </a> was used. This dataset contained various data on Covid Cases, Deaths, Testing and Vaccinations. The period chosen was January 1st, 2020 to November 21st, 2022. 

## Tools Used

1. Excel
2. Microsoft SQL Server Management Studio
3. Tableau

## Data Transformations

The data used for the purpose of this analysis were:

1. Testing for Infections
2. Postivity Rates
3. Death Rates

As part of the Data Cleaning process, several records in the data had fields with null values which needed to be changed to '0' for performing various mathematical calculations on them. Most of these null values were in January and February 2020. The below fields were changed from null to '0' using SQL:

1. total_cases
2. new_cases
3. total_deaths
4. new_deaths
5. total_tests
6. new_tests
7. total_tests_per_thousand
8. new_tests_per_thousand
9. positive_rate
10. tests_per_case

The below SQL queries were performed for changing the above fields:

    update ProjectPortfolio..[Covid Deaths]
    set total_cases = '0'
    where total_cases is null;

    update ProjectPortfolio..[Covid Deaths]
    set new_cases = '0'
    where new_cases is null;

    update ProjectPortfolio..[Covid Deaths]
    set total_deaths = '0'
    where total_deaths is null;

    update ProjectPortfolio..[Covid Deaths]
    set new_deaths = '0'
    where new_deaths is null;

    update ProjectPortfolio..[Covid Vaccinations]
    set total_tests = '0'
    where total_tests is null;

    update ProjectPortfolio..[Covid Vaccinations]
    set new_tests = '0'
    where new_tests is null;

    update ProjectPortfolio..[Covid Vaccinations]
    set total_tests_per_thousand = '0'
    where total_tests_per_thousand is null;

    update ProjectPortfolio..[Covid Vaccinations]
    set new_tests_per_thousand = '0'
    where new_tests_per_thousand is null;

    update ProjectPortfolio..[Covid Vaccinations]
    set positive_rate = '0'
    where positive_rate is null;

    update ProjectPortfolio..[Covid Vaccinations]
    set tests_per_case = '0'
    where tests_per_case is null;

## Analysis

Using SQL Server Management Studio, the following were extracted:

    (i) Testing % - Percentage of the Population Tested for Covid
    (ii) Covid Case % - Percentage of the Population to have Contracted Covid
    (iii) Covid Positivity % - Percentage of Infections Among Those Who were Tested
    (iv) Covid Death % - Percentage of Deaths Among Those Who Contracted Covid

2. The queries used to extract the above data are available in the <a href = "https://github.com/rahulshankariyer/Portfolio/blob/main/Covid-19%20Testing%2C%20Infection%20%26%20Death%20Rates/Covid%20Testing%2C%20Cases%20%26%20Deaths.sql"> Covid Testing, Cases & Deaths.sql </a> file 

3. Using the data extracted in Step 2, 3 visualizations were created in Tableau - 
    
    <b> a. Testing % - USA vs Rest of the World </b>
    ![alt text](https://raw.githubusercontent.com/rahulshankariyer/Covid19_Tests_Cases_and_Deaths/main/Testing%20%25%20-%20USA%20vs%20World.png)
    
    <b> b. Covid Case % - USA vs Rest of the World </b>
    ![alt text](https://raw.githubusercontent.com/rahulshankariyer/Covid19_Tests_Cases_and_Deaths/main/Covid%20Case%20%25%20-%20USA%20vs%20World.png)
    
    <b> c. Tests Per Case - USA vs Rest of the World </b>
    ![alt text](https://raw.githubusercontent.com/rahulshankariyer/Covid19_Tests_Cases_and_Deaths/main/Tests%20Per%20Case%20-%20USA%20vs%20Rest%20of%20the%20World.png)
    
    <b> d. Covid Death % - USA vs Rest of the World </b>
    ![alt text](https://raw.githubusercontent.com/rahulshankariyer/Covid19_Tests_Cases_and_Deaths/main/Covid%20Death%20%25%20-%20USA%20vs%20World.png)
    
## Insights

From the above data, the following insights were gathered:

1. USA had a Covid Positive Rate of 10.77% while the Rest of the World had 12.94%, ie, USA conducted 9.28 Tests Per Case while the Rest of the World conducted 7.73 Tests Per Case
2. USA ranks #24 in the World in Testing % of the Population (from high to low), with 270% of the population tested. The Rest of the World comes in with 183% in comparison.
3. Since the virus began to spread, USA has consistently tested a higher percentage of its population than the Rest of the World has from March 2020 through to July 2022.
4. USA ranks #57 in the World in Covid % of the Population (from high to low), with 29.07% contracting the virus. The Rest of the World comes in with 7% in comparison.
5. Since the virus began to spread, the percentage of Covid Cases in the USA has consistently increased at a more rapid pace than that of the Rest of the World. 
6. USA ranks #24 in the World in Death % among Covid Positive Cases (from high to low), with 1.02% of them dying of the virus. The Rest of the World comes in with 1.03% in comparison.
7. Since the virus began to spread, the percentage of Covid Deaths in the USA has overall increased and decreased at a similar rate with that of the Rest of the world, sometimes going above and sometimes going below.

## Conclusions

1. USA was more efficient than the Rest of the World in Testing & detecting Covid Positive Cases.
2. USA couldn't control the spread of the virus very well, but they were able to control the death rate better than most other countries in the world.

## Accuracy of the Insights & Conclusions

The accuracy is moderate for the following reasons:

1. The reporting of data in many countries were not reliable. Eg. North Korea and China.
2. The level of vaccinations varied from country to country.
3. The efficacies of different vaccines were different.

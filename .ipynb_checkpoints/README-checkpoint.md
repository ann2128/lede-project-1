{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "9e3c7516",
   "metadata": {},
   "source": [
    "# Mapping Community Gardens in NYC  \n",
    "\n",
    "Summer is a great time to be out in a garden! With that, I wanted to research communtiy gardens and find out where they are located. I also wanted to see if there are any trends to the hundreds of gardens that exist throughout New York, such as which borough has most of the city's community gardens or which neighbourhood is more likely to have one.\n",
    "\n",
    "Here is the story's [webpage]( ).\n",
    "\n",
    "### Main Findings\n",
    " - There are 541 active community gardens in New York City as of this month. \n",
    " - But the gardens are not distributed equally across the five boroughs. Brooklyn, the most populous borough, has 238 gardens — close to half of the city's total number. This also means 9.24 per 100,000 Brooklyn residents have access to a garden.  \n",
    " - Queens, the second-most populous borough, has the second-lowest numbers of garden at 43. This means 1.89 people per 100,000 Queens residents have access to a garden — almost 5 times lower than in Brooklyn.\n",
    " - Staten Island, the least populous borough, has the lowest number of gardens at 7. \n",
    " - Most community gardens in NYC are located in lower-income neighborhoods, with more than half of them locating in ZIP codes with median household income below $53,000. Lower-income ZIP codes are also slightly more likely to have a higher number of active gardens within their boundaries.\n",
    " - I didn't have time to fully analyze the racial data, so I only looked at the 10 ZIP codes with the highest numbers of community gardens. Ranging from 17 to 44 gardens, these big clusters  tend to be in neighborhoods of color, such as predominantly Black neighborhoods. The only exception is ZIP code 10009 in the East Village, whose population is around 51% White (non-Hispanic/Latino). \n",
    " \n",
    "### Methodology \n",
    "\n",
    "My [main dataset](https://data.cityofnewyork.us/dataset/GreenThumb-Garden-Info/p78i-pat6) came from Open NYC in a CSV file. It provides me with information for around 550 community gardens, their status, as well as the borough and ZIP code they are located in. I then supplemented it with demographic data I got from US Census for [individual boroughs](https://www.census.gov/quickfacts/fact/table/richmondcountynewyork,queenscountynewyork,newyorkcountynewyork,kingscountynewyork,bronxcountynewyork/PST045222) and [relevant ZIP codes](https://data.census.gov/table?y=2021&d=ACS+5-Year+Estimates+Data+Profiles). For indvidiual boroughs, I collected population data. For individual ZIP codes, I collected data on their population, median household income, median age and racial makeup. I pulled these datapoints individually instead of scraping through the websites.\n",
    "\n",
    "I used pandas to analyze the datasets. I mostly tried to count, rank and sort the individual datapoints for outliers or interesting trends, such as Queens having the second-lowest number of gardens in NYC. I also calulcated the garden-to-population ratio by calculating the number of garden of each borough or zipcode with the population numbers I pulled from other websites. \n",
    "\n",
    "Here are the CSV files:\n",
    " - [Open NYC Community Garden]( )\n",
    " - [Basic analysis]( )\n",
    " - [Borough analysis]( )\n",
    " - [ZIP code analysis]( )\n",
    "\n",
    "I then used datawrapper to make all of my charts, including the map. \n",
    "\n",
    "### New Skills\n",
    "\n",
    "I got better with using pandas to analyze data, especially with adding and removing columns. I also got more comfortable saving a chunk of dataset as a new csv file, as I tried to think ahead of how to do the data visualization. I also got to practice using Datawrapper to make maps and charts. I think I grew the most in terms of figuring out what is worth visualizing and which chart format is best at doing so.\n",
    "\n",
    "### What Else To Try\n",
    "\n",
    "I would have liked to be able to scrape the US Census Bureau's website in order to pull the demographic data, instead of having to manually pull them one by one for each borough and ZIP code. And since I have no idea what that entails, I also don't know if scraping would make the process faster in this case. \n",
    "\n",
    "With more time, I would also have liked to pull data for the ZIP codes without an active community garden so that I could conclusively analyze them for trends, such as which kind of neighbourhood is more likely to have one."
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.10.11"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}

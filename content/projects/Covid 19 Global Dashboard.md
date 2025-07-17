+++
title = "COVID-19 Global Dashboard"
draft = false
showReadingTime = false
showWordCount = false
tags = ["Tableau", "Dashboard", "Visualization"]
summary = "An interactive Tableau dashboard visualizing global COVID-19 confirmed cases and deaths over time with geospatial and trend visualizations."
ShowToc = false

[cover]
  image = "/images/covid1.jpg"

+++

## Overview

This interactive **Tableau dashboard** provides insights into the global spread of **COVID-19** by visualizing confirmed cases and deaths over time. It includes geospatial and temporal analyses across countries.

## Tools Used

- **Tableau Desktop**
- **Data Source:** Public COVID-19 dataset

## Features

- Global **bubble map** sized by confirmed cases
- Time-series **line charts** of:
  - Confirmed cases
  - Confirmed deaths
- **Top 10 countries** ranked by:
  - Total confirmed cases
  - Total confirmed deaths
- **Date filter** to explore trends over time
- Interactive tooltips and filterable elements

## Dashboard Components

| Component        | Description                                      |
| ---------------- | ------------------------------------------------ |
| Map              | Bubble map showing confirmed global cases        |
| Confirmed Cases  | Cumulative line chart with interactive tooltip   |
| Confirmed Deaths | Line chart showing confirmed deaths over time    |
| Top Countries    | Bar charts for top 10 countries (cases & deaths) |

## Data Preparation

- Standardized country name formats
- Parsed and aggregated daily records by country and date
- Calculated cumulative case and death metrics
- Generated dynamic rankings for top 10 charts

## How to Use

1. Open the `.twbx` workbook in **Tableau Desktop**
2. Use the **date slider** to filter time windows
3. Hover over charts for **detailed tooltips**
4. Use filters to explore **specific countries or regions**

[View More Details](https://github.com/ritaliiii/COVID-19-Global-Dashboard-Tableau-)

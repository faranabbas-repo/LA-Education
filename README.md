# Educational Attainment in Los Angeles County

[![Data Source](https://img.shields.io/badge/Data-U.S.%20Census%20ACS-blue?style=flat)](https://www.census.gov/programs-surveys/acs)

Spatial public-policy and education-economics project mapping bachelor's degree attainment across Los Angeles County census tracts.

This repository is designed as a portfolio-ready Quarto project. It uses tract-level American Community Survey data to show how educational attainment varies across neighborhoods, with a focus on local inequality, human capital, and place-based opportunity.

## Project Snapshot

- Topic: Educational attainment and geographic inequality
- Geography: Los Angeles County census tracts
- Data source: American Community Survey 5-year estimates
- Main variable: Share of residents with a bachelor's degree
- Tools: R, tidycensus, sf, ggplot2, leaflet, Quarto

## Research Question

How uneven is bachelor's degree attainment across neighborhoods in Los Angeles County?

This project frames education as a spatial inequality question. Differences in educational attainment can reveal broader differences in opportunity, income potential, labor-market access, and long-run human capital across local areas.

## Why This Project Matters

Education is central to labor economics, regional inequality, and public policy. A tract-level map makes those differences visible in a way that aggregate county averages cannot.

For an economics portfolio, this repo demonstrates the ability to:

- work with official U.S. micro-regional data
- retrieve Census data in R using the ACS API
- construct tract-level indicators
- build both static and interactive maps
- connect place-based patterns to human-capital and inequality questions

## Data

Source: U.S. Census Bureau American Community Survey (ACS) 5-year estimates via `tidycensus`

Current variable setup:

- `B15003_022`: Number of residents with a bachelor's degree
- `B15003_001`: Total educational attainment population in the table universe

The project uses these variables to compute:

- bachelor's degree share by census tract in Los Angeles County

## Analytical Approach

The project:

- pulls tract-level ACS data for Los Angeles County
- reshapes the data into a usable tract dataset
- computes the percentage of residents with a bachelor's degree
- visualizes the results as both a static choropleth and an interactive leaflet map

This is an exploratory spatial analysis rather than a causal design, but it creates a strong foundation for future extensions such as:

- linking education to income or rent patterns
- comparing attainment across racial or income groups
- studying spatial clustering of opportunity
- building a policy dashboard on neighborhood inequality

## Privacy and Reproducibility Note

The source code now expects a Census API key through the `CENSUS_API_KEY` environment variable instead of hardcoding the key inside the repository.

Example setup in R:

```r
Sys.setenv(CENSUS_API_KEY = "your_key_here")
```

## Current Project Structure

- `index.qmd` for the main map-based analysis
- `sources.qmd` for data notes and variable definitions
- `about.qmd` for project context
- `_quarto.yml` for website configuration
- `styles.css` for basic styling

## Portfolio Value

This repo strengthens an economics CV because it shows that you can turn a public-policy topic into tract-level spatial analysis with real data and clear interpretation.

A concise CV description for this project could be:

> Built a tract-level education inequality project using American Community Survey data in R, mapping bachelor's degree attainment across Los Angeles County with static and interactive visualizations.

## Reproducibility

Install the required R packages:

```r
install.packages(c("tidycensus", "tidyverse", "sf", "ggplot2", "leaflet"))
```

Then set `CENSUS_API_KEY` in your environment and render the site locally with Quarto.

## Author

Faran Abbas
Graduate Student, World Economy, Shandong University

- Email: [faranabbas@hotmail.com](mailto:faranabbas@hotmail.com)
- GitHub: [faranabbas-repo](https://github.com/faranabbas-repo)

## Acknowledgment

This project is part of a broader effort to build a stronger economics portfolio with real-world data projects.

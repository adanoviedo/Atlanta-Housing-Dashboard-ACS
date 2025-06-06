# 🏠 Atlanta Housing Dashboard - ACS Census Data

This project is a **Shiny-powered interactive dashboard** built with `flexdashboard` that visualizes housing-related data from the **American Community Survey (ACS) 5-Year Estimates (2023)** for the **Atlanta metropolitan area**. It allows users to explore **housing affordability** and **rental trends** across key counties: **Fulton, DeKalb, Cobb, Gwinnett, and Clayton**.

## ⚠️ Disclaimer

This dashboard is intended for **educational and demonstration purposes** only. While data is pulled directly from the U.S. Census Bureau, no modeling or contextual interpretation has been performed. Do not use for drawing conclusions for policy, investment, or planning purposes.

## 📊 Features

### 🗺️ Median Home Values by Census Tract
Displays an interactive map of median home values across census tracts. Users can click on any tract to view values and margins of error.

### ⚖️ Rent vs. Ownership Affordability
Visualizes whether it's more affordable to rent or own in each tract, based on a ratio of median contract rent to median monthly ownership costs. The map is color-coded to indicate affordability tiers.

### 🛏️ Median Rent by Number of Bedrooms
A suite of tools lets users explore **rental costs by bedroom size**, with:
- An interactive map filtered by bedroom count
- A boxplot comparing median rent by **county**
- A strip (quasirandom) plot showing rental distribution by **bedroom size**

## 📦 Built With

- **R packages**:  
  `flexdashboard`, `shiny`, `tidyverse`, `tidycensus`, `leaflet`, `mapview`, `ggbeeswarm`, `viridis`, `biscale`, `scales`, `tigris`

- **Data Source**:  
  [U.S. Census Bureau - American Community Survey (ACS)](https://www.census.gov/programs-surveys/acs)

## 📌 ACS Variables Used

| Variable Code  | Description                                    |
|----------------|------------------------------------------------|
| B25077_001     | Median home value (owner-occupied units)       |
| B25031_003–007 | Median gross rent by bedroom count (1–5+)      |
| B25058_001     | Median contract rent (excluding utilities)     |
| B25105_001     | Median monthly ownership costs (all expenses)  |

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/adanoviedo/Atlanta_Housing_ACS.git
   ```

2. **Install the required R packages**
   ```r
   install.packages(c(
     "flexdashboard", "shiny", "tidyverse", "tidycensus", "mapview", 
     "leaflet", "scales", "tigris", "ggbeeswarm", "biscale", "viridis"
   ))
   ```

3. **Set your Census API key**
   ```r
   library(tidycensus)
   census_api_key("YOUR_API_KEY_HERE", install = TRUE)
   ```

4. **Open the dashboard**
   - Open `census_dashboard_atlanta.Rmd` in RStudio
   - Click **Run Document** or **Run App**

## 🗒️ Notes

- The dashboard uses **ACS 5-Year 2023 estimates**, which offer stability at smaller geographic levels like census tracts.
- Ensure that `tigris_use_cache = TRUE` is set to avoid repeated shapefile downloads.

## 📫 Contact

If you have questions or suggestions, feel free to reach out via GitHub!

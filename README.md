# 📊 Indonesia GDP Analysis by Province

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Tableau](https://img.shields.io/badge/Tableau-Public-orange.svg)](https://public.tableau.com/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green.svg)](https://pandas.pydata.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> A comprehensive data engineering project analyzing Indonesia's provincial GDP distribution through web scraping, data processing, and interactive visualization.

**🎯 Part of DataSeriesFair 4.0 Challenge by [Dibimbing.id](https://dibimbing.id)**

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Technology Stack](#-technology-stack)
- [Project Structure](#-project-structure)
- [Installation & Setup](#-installation--setup)
- [Data Pipeline & Methodology](#-data-pipeline--methodology)
- [Interactive Dashboard](#-interactive-dashboard)
- [Key Findings](#-key-findings)
- [Data Source](#-data-source)
- [Resources](#-resources)
- [Future Improvements](#-future-improvements)
- [Acknowledgments](#-acknowledgments)

---

## 🎯 Overview

This project analyzes the **Gross Domestic Product (GDP)** distribution across Indonesian provinces to identify economic patterns and regional disparities. The analysis provides insights into which provinces contribute most significantly to Indonesia's economy and reveals the economic concentration in specific regions.

**Project Objectives:**
- Extract and process provincial GDP data from reliable sources
- Enrich data with geographic coordinates for spatial analysis
- Create interactive visualizations for data exploration
- Identify top-performing provinces and regional economic patterns
- Present findings through a professional Tableau dashboard

---

## ✨ Features

- **🕷️ Automated Web Scraping**: Extracts GDP data from Wikipedia using BeautifulSoup
- **🧹 Data Processing Pipeline**: Cleans and transforms raw data into analysis-ready format
- **🌍 Geographic Enrichment**: Adds latitude/longitude coordinates for each province
- **📊 Interactive Visualization**: Tableau dashboard with multiple views and filters
- **📈 Economic Analysis**: Identifies patterns in regional GDP distribution
- **💾 Exportable Dataset**: Clean CSV output for further analysis

---

## 🛠️ Technology Stack

### Data Collection & Processing
- **Python 3.x** - Core programming language
- **requests** - HTTP library for web scraping
- **BeautifulSoup4** - HTML parsing and data extraction
- **pandas** - Data manipulation and analysis

### Visualization
- **Tableau Public** - Interactive dashboard creation

### Data Source
- **Wikipedia** - List of Indonesian provinces by GDP

---

## 📁 Project Structure

```
twb-indonesia-gdp/
│
├── data_engineer.ipynb          # Jupyter notebook with complete data pipeline
├── indonesian_gdp.csv           # Processed dataset with 34 provinces
├── Indonesia GDP.twb            # Tableau workbook file
└── README.md                    # Project documentation
```

**File Descriptions:**
- `data_engineer.ipynb`: Contains the complete workflow from web scraping to data export
- `indonesian_gdp.csv`: Final dataset with GDP figures and geographic coordinates
- `Indonesia GDP.twb`: Tableau workbook with interactive visualizations

---

## 🚀 Installation & Setup

### Prerequisites
- Python 3.x installed on your system
- Jupyter Notebook or Google Colab
- Tableau Public (for viewing/editing the dashboard)

### Required Python Packages

```bash
pip install requests beautifulsoup4 pandas
```

### Running the Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/Chanzwastaken/twb-indonesia-gdp.git
   cd twb-indonesia-gdp
   ```

2. **Open the Jupyter Notebook**
   ```bash
   jupyter notebook data_engineer.ipynb
   ```
   
   *Or open in Google Colab:*
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Chanzwastaken/indonesia-gdp/blob/main/data_engineer.ipynb)

3. **Run all cells** to execute the complete pipeline:
   - Web scraping
   - Data cleaning
   - Geographic enrichment
   - CSV export

4. **View the dashboard** in Tableau Public (link below)

---

## 🔄 Data Pipeline & Methodology

### Step 1: Data Extraction
- Target URL: [Wikipedia - List of Indonesian Provinces by GDP](https://en.wikipedia.org/wiki/List_of_Indonesian_provinces_by_GDP)
- Extract table data using BeautifulSoup
- Parse HTML table structure to retrieve GDP figures

### Step 2: Data Cleaning & Transformation
- Remove header rows and aggregate entries
- Filter to include only 34 individual provinces
- Clean numeric values (remove commas, convert to appropriate types)
- Standardize column names for consistency

### Step 3: Data Enrichment
- Add geographic coordinates (latitude/longitude) for each province
- Create combined lat/long field for mapping
- Categorize provinces by major regions (Java, Sumatra, Kalimantan, etc.)

### Step 4: Data Export
- Export cleaned dataset to CSV format
- Validate data completeness and accuracy
- Prepare for Tableau visualization

### Data Schema

| Column | Description | Example |
|--------|-------------|---------|
| `rank` | Provincial GDP ranking | 1 |
| `province` | Province name | Jakarta |
| `region` | Major island/region | Java |
| `gdp_in_billion_rp` | GDP in billion Indonesian Rupiah | 3,186,470 |
| `gdp_in_billion_usd` | GDP in billion USD (nominal) | 214.59 |
| `gdp_ppp_in_billion_usd` | GDP in billion USD (PPP) | 669.63 |
| `latitude` | Geographic latitude | -6.175247 |
| `longitude` | Geographic longitude | 106.8270488 |
| `lat_long` | Combined coordinates | -6.175247 106.8270488 |

---

## 📊 Interactive Dashboard

### 🔗 [View Live Dashboard on Tableau Public](https://public.tableau.com/views/IndonesiaGDP_17046746539830/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link)

The interactive dashboard features:
- **Geographic Map**: Visualize GDP distribution across Indonesia
- **Bar Charts**: Compare provincial GDP rankings
- **Regional Analysis**: Filter by major island regions
- **Tooltips**: Hover for detailed province information
- **Dynamic Filtering**: Explore data interactively

*Click the link above to explore the full interactive experience!*

---

## 💡 Key Findings

### Top 3 Provinces by GDP

1. **🥇 Jakarta** (Capital City)
   - GDP: **3,186,470 billion IDR** (~214.59 billion USD)
   - Represents Indonesia's economic and political center
   - Significantly higher GDP than any other province

2. **🥈 East Java**
   - GDP: **2,730,907 billion IDR** (~183.91 billion USD)
   - Major industrial and commercial hub
   - Second-largest contributor to national economy

3. **🥉 West Java**
   - GDP: **2,422,782 billion IDR** (~163.16 billion USD)
   - Dense population and industrial activity
   - Strategic location near Jakarta

### Regional Economic Patterns

#### 🏝️ **Java Island Dominance**
- **All top 3 provinces** are located in Java
- Java Island accounts for the **majority of Indonesia's GDP**
- Indicates significant economic concentration in this region

#### 🌴 **Sumatra's Strong Performance**
- **Riau** (4th), **North Sumatra** (5th), and **South Sumatra** (6th) rank highly
- Resource-rich provinces with oil, gas, and plantation industries
- Second-most economically significant region after Java

#### 🌊 **Regional Disparities**
- Clear economic divide between western and eastern Indonesia
- Java and Sumatra dominate the top 10 rankings
- Eastern provinces (Papua, Maluku, Nusa Tenggara) show lower GDP figures

### Economic Insights

- **Geographic Concentration**: Economic activity is heavily concentrated in Java and Sumatra
- **Urban Centers**: Provinces with major cities (Jakarta, Surabaya, Bandung) show highest GDP
- **Resource Wealth**: Provinces rich in natural resources (Riau, East Kalimantan) perform well
- **Development Gap**: Significant disparity between western and eastern Indonesian provinces

---

## 📚 Data Source

**Primary Source:**
- [Wikipedia - List of Indonesian Provinces by GDP](https://en.wikipedia.org/wiki/List_of_Indonesian_provinces_by_GDP)
- Data represents 2022 GDP figures
- Includes nominal GDP and PPP-adjusted values

**Data Attribution:**
- GDP figures sourced from official Indonesian statistics
- Geographic coordinates from standard mapping databases
- All data processed and verified for accuracy

---

## 📖 Resources

- **📊 Presentation Slides**: [View on Canva](https://www.canva.com/design/DAF5QIzle4A/8Ugb3AoUaq2_6_mdjaBKyw/view?utm_content=DAF5QIzle4A&utm_campaign=designshare&utm_medium=link&utm_source=editor)
- **📄 Challenge Documentation**: [DataSeriesFair 4.0 PDF](https://drive.google.com/file/d/1bfAlt4rdr5laB8Gil2oOc51rlOzmmsl3/view?usp=drive_link)
- **💻 Google Colab Notebook**: [Open in Colab](https://colab.research.google.com/github/Chanzwastaken/indonesia-gdp/blob/main/data_engineer.ipynb)

---

## 🚀 Future Improvements

- [ ] **Time Series Analysis**: Track GDP changes over multiple years
- [ ] **Per Capita GDP**: Calculate and visualize GDP per capita by province
- [ ] **Sector Breakdown**: Analyze GDP by economic sectors (agriculture, manufacturing, services)
- [ ] **Correlation Analysis**: Explore relationships between GDP and other factors (population, infrastructure)
- [ ] **Predictive Modeling**: Forecast future GDP trends using machine learning
- [ ] **Automated Updates**: Schedule periodic data refreshes from source
- [ ] **Additional Visualizations**: Create more chart types (treemaps, heatmaps, scatter plots)
- [ ] **Mobile Dashboard**: Optimize Tableau dashboard for mobile viewing

---

## 🙏 Acknowledgments

- **[Dibimbing.id](https://dibimbing.id)** - For organizing the DataSeriesFair 4.0 challenge
- **Wikipedia Contributors** - For maintaining comprehensive GDP data
- **Tableau Public** - For providing free visualization platform
- **Python Community** - For excellent data processing libraries

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👤 Author

**Chanzwastaken**

- GitHub: [@Chanzwastaken](https://github.com/Chanzwastaken)
- Project Link: [twb-indonesia-gdp](https://github.com/Chanzwastaken/twb-indonesia-gdp)

---

<div align="center">

**⭐ If you found this project helpful, please consider giving it a star!**

Made with ❤️ for DataSeriesFair 4.0

</div>

# FME Datathon 2023 - Sustainable UPC Challenge 🚲🌱

## Sustainable Mobility Analysis at UPC

This project was developed for the **FME Datathon 2023**, specifically for the **Sustainable UPC Challenge**. The main objective is to analyze mobility patterns of students at Universitat Politècnica de Catalunya (UPC) and provide insights to promote more sustainable transportation.

## 📊 Project Description

The project analyzes UPC student mobility data to understand:
- **Transportation patterns**: How students commute between their homes and different UPC campuses
- **Mobility preferences**: What factors influence transportation mode choice
- **Environmental impact**: Analysis of the sustainability of different transportation modes used
- **Existing infrastructure**: Mapping of public transportation and bicycle infrastructure

## 🗂️ Project Structure

```
├── data/
│   ├── preprocessed.csv              # Main processed data
│   ├── preprocessed_co2.csv          # Data with CO2 metrics
│   ├── bicis_coordenades.csv         # Bicycle station coordinates
│   └── coordenades2.csv              # Transportation geospatial data
├── src/
│   ├── preprocessing.ipynb           # Data cleaning and preprocessing
│   ├── insights.ipynb                # Statistical analysis and correlations
│   └── plotting.ipynb                # Visualizations and interactive maps
└── visualisation/
    ├── HTML/                         # Generated interactive maps
    │   ├── heatmap.html
    │   ├── circle_lines.html
    │   └── pt_lines.html
    └── PNG/                          # Static graphics
        ├── heatmap.png
        ├── metro_bike_transportation.png
        └── pt_lines.png
```

## 🔧 Technologies Used

- **Python**: Main analysis language
- **Pandas**: Data manipulation and analysis
- **Folium**: Interactive geospatial visualizations
- **Matplotlib/Seaborn**: Statistical graphics
- **Shapely**: Geometric data processing
- **Scipy**: Advanced statistical analysis

## 📈 Main Analysis

### 1. Transportation Categorization
Transportation modes were categorized into three groups:
- ** Private Transport**: Combustion vehicles, electric vehicles, motorcycles, taxis
- ** Public Transport**: Metro, bus, train (Renfe), FGC, tram
- ** Active Transport**: Walking, bicycle

### 2. Decision Factors
The reasons why students choose each transportation mode were analyzed:
- Speed (`r_fastest`)
- Economy (`r_cheapest`) 
- Comfort (`r_confortable`)
- Only available option (`r_onlyoption`)
- Environmental reasons (`r_environmental`)
- Health (`r_healthiest`)
- Need for private transport (`r_needprivate`)

### 3. Geospatial Analysis
- **Heat maps**: Student distribution by postal code
- **Main routes**: Most used connections between residences and UPC campuses
- **Infrastructure**: Location of bicycle stations and public transport
- **Temporal analysis**: Travel time estimation according to transportation mode

## 🗺️ Main Visualizations

### Interactive Maps
1. **Heat Map**: Shows student density by geographical area
2. **Flow Map**: Visualizes the most popular routes with arrows proportional to number of users
3. **Infrastructure**: Shows bicycle stations, metro stops and public transport routes

### Statistical Analysis
- **Correlation matrix**: Relationships between different decision factors
- **Distribution by campus**: Analysis of transport preferences by UPC campus
- **Demographic segmentation**: Patterns according to gender, year of study, etc.

## 🏃‍♂️ How to Run the Project

### Requirements
```bash
pip install pandas numpy matplotlib seaborn folium shapely branca scipy
```

### Execution
1. **Preprocessing**: Run `src/preprocessing.ipynb`
2. **Analysis**: Run `src/insights.ipynb`
3. **Visualizations**: Run `src/plotting.ipynb`

## 📊 Key Findings

### Transportation Distribution
- **37.2%** of trips use active transport
- **43.4%** use public transport
- **19.4%** use private transport

### Most Influential Factors
1. **Speed**: Most valued factor by students
2. **Comfort**: Second most important factor
3. **Environmental considerations**: Lower influence on decision

### Geographic Patterns
- Greater use of public transport in well-connected areas
- Private transport predominant in peripheral areas
- Active transport popular for short distances to Barcelona city center

## 🎯 Impact and Recommendations

### For Sustainability
1. **Promotion of active transport** for short distances
2. **Improvement of public transport connections** from areas with high private transport dependency
3. **Incentives** for the use of sustainable transportation modes

### For Infrastructure
1. **Expansion of bicycle network** on popular routes
2. **Optimization of public transport schedules** according to student patterns
3. **Modal interchange points** strategically located

## 👥 Team

Project developed as part of FME Datathon 2023 - Sustainable UPC Challenge.
- Albert Gómez
- Amadeu Moya
- Jordi G.B
- Miquel Rodríguez
---

*🌍 Contributing to a more sustainable future through data analysis* 🌱

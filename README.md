# Zero Ghibli: Studio Ghibli Film Analysis

This project provides a comprehensive analysis of Studio Ghibli films using data science techniques. By examining various aspects of these beloved animated films, we aim to uncover patterns, trends, and insights about their storytelling, themes, and reception.

## Project Overview

This repository contains:

- A Jupyter Notebook (`ghibli_analysis.ipynb`) with all data analysis code and visualizations
- Documentation of methodology and findings (`ghibli_project_documentation.pdf`)
- Dataset sources and processing techniques
- Visualization outputs and statistical models

## Features

- Exploratory data analysis of Studio Ghibli films
- Visualization of key metrics and trends
- Statistical analysis of film characteristics
- Predictive modeling of film success factors
- Thematic analysis of recurring motifs in Ghibli storytelling
- Comparative analysis with other animation studios

## Methodology

The analysis follows these key steps:

1. **Data Collection**: Gathering film data from multiple sources
2. **Data Cleaning**: Handling missing values and standardizing formats
3. **Exploratory Analysis**: Identifying patterns and relationships
4. **Statistical Testing**: Validating hypotheses about film characteristics
5. **Visualization**: Creating insightful plots and interactive dashboards
6. **Interpretation**: Drawing conclusions about Ghibli's filmmaking approach

## Datasets

The analysis combines several datasets to create a comprehensive view of Studio Ghibli films:

### Primary Datasets
- **Studio Ghibli API Data**: Core information about each film including title, director, release date, running time, and synopsis (accessed via [https://ghibliapi.herokuapp.com](https://ghibliapi.herokuapp.com))
- **Box Office Performance**: Revenue data from The Numbers and Box Office Mojo, including domestic and international earnings
- **Critical Reception**: Review scores aggregated from Metacritic, Rotten Tomatoes, and IMDb
- **Award Information**: Data on nominations and wins for major awards (Academy Awards, Annie Awards, Japan Academy Film Prize)

### Supplementary Datasets
- **Character Analysis**: Information about main and supporting characters, their roles and development
- **Thematic Elements**: Curated dataset tracking recurring themes across films (environmentalism, coming-of-age, etc.)
- **Visual Style Metrics**: Quantitative data about color palettes, animation techniques, and visual compositions
- **Audience Demographics**: Viewership data by age, region, and gender when available

All datasets were cleaned, merged, and processed to create a unified analytical framework.

## Key Findings

Some notable insights from our analysis include:

- Correlation between specific thematic elements and critical reception
- Trends in visual styling across different directors' works
- The evolution of Studio Ghibli's storytelling approach over time
- Comparative success factors between Ghibli films and other major animation studios
- Audience demographic patterns and their relationship to film themes

For detailed findings, please refer to the Jupyter notebook and documentation.

## Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook
- Required libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

### Installation

```bash
git clone https://github.com/filberthamijoyo/zero-ghibli.git
cd zero-ghibli
pip install -r requirements.txt
```

### Running the Analysis

Open the Jupyter notebook to explore the analysis:

```bash
jupyter notebook ghibli_analysis.ipynb
```

## Visualizations

The project includes various visualization types:

- Time series analysis of film performance
- Correlation heatmaps of film attributes
- Network graphs of character relationships
- Thematic radar charts comparing different films
- Geographic distribution of box office performance

## Future Work

Potential extensions to this analysis include:

- Deeper natural language processing of film dialogues
- Expanded comparison with other animation studios
- Machine learning models to predict film success
- Interactive web dashboard for exploring the data

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Studio Ghibli for their incredible filmmaking
- Data sources that made this analysis possible
- Contributors to the open-source libraries used in this project
- The animation research community for methodological inspiration 
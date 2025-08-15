# World's Largest Economies Data Extractor

A Python project that extracts GDP data from Wikipedia's "List of countries by GDP (nominal)" page and processes it into a clean CSV format.

## Overview

This project scrapes GDP data for the world's largest economies from a Wikipedia archive page and processes the data to create a clean dataset showing the top 10 countries by GDP in billions USD.

## Features

- Web scraping from Wikipedia using pandas
- Data cleaning and transformation
- Convert GDP from millions to billions USD
- Export to CSV format
- Error handling and warnings suppression

## Requirements

```
pandas>=2.0.0
numpy>=1.24.0
lxml>=4.9.0
html5lib>=1.1
beautifulsoup4>=4.11.0
requests>=2.28.0
```


### Sample Output:
```
Country,GDP (Billion USD)
United States,26854.60
China,19373.59
Japan,4409.74
Germany,4308.85
India,3736.88
United Kingdom,3158.94
France,2923.49
Italy,2169.74
Canada,2089.67
Brazil,2081.24
```

## Data Source

Data is extracted from the Internet Archive snapshot of Wikipedia's "List of countries by GDP (nominal)" page:
- Source: https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29
- Archive Date: September 2, 2023

## Project Structure

```
gdp-data-extractor/
├── README.md
├── requirements.txt
├── gdp_extractor.py
├── data_visualization.py
├── Largest_economies.csv
└── .gitignore
```

## Visualization

The project includes an optional visualization script (`data_visualization.py`) that creates:
- Bar chart of top 10 economies
- Pie chart showing GDP distribution
- GDP comparison charts

To run visualizations:
```bash
python data_visualization.py
```

## Technical Details

### Data Processing Steps:
1. Suppress warnings for cleaner output
2. Extract HTML tables using `pd.read_html()`
3. Select the appropriate table (index 3)
4. Clean column names and select relevant columns
5. Filter to top 10 countries
6. Convert GDP from millions to billions
7. Round to 2 decimal places
8. Export to CSV

### Error Handling:
- Network connectivity issues
- Missing dependencies
- Data structure changes

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## Acknowledgments

- Data source: Wikipedia
- Python libraries: pandas, numpy, lxml
- Internet Archive for data preservation

## Future Enhancements

- [ ] Add historical GDP data tracking
- [ ] Include more economic indicators
- [ ] Add data validation checks
- [ ] Create interactive dashboard
- [ ] Add automated data updates
- [ ] Include GDP per capita analysis

## Contact

Created by Zen - feel free to contact me on zenithwijeratna@gmail.com

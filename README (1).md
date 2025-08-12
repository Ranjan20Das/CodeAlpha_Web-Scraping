# Web Scraping Dataset Analyzer

This Python project allows you to **analyze datasets** — with special handling for **quote datasets** (with `quote`, `author`, `tags` columns) and generic datasets.  
It performs statistical summaries, visualizations, and word cloud generation.

---

## Features

### For Quotes Dataset
- **Basic Statistics**
  - Total quotes, unique authors, average words per quote
  - Longest and shortest quotes
- **Author Analysis**
  - Top authors by quote count
- **Tag Analysis**
  - Most common tags
- **Visualizations**
  - Distribution of quote lengths
  - Top authors bar chart
  - Top tags bar chart
  - Quotes per page (if `page` column exists)
- **Word Cloud**
  - Visual representation of most frequent words in quotes

---

### For Generic Dataset
- **Basic Statistics**
  - Row and column count
  - Summary of all columns
- **Visualizations**
  - Numeric column distribution
  - Top values in a categorical column
  - Correlation heatmap (if numeric columns > 1)
  - Row index distribution
- **Word Cloud**
  - Generated from the first text column

---

## Project Structure
```
├── analyzer.py           # Main Python script
├── data_kaggle.csv       # Example dataset (optional)
├── processed_dataset.csv # Output after analysis
└── README.md             # Documentation
```

---

## Installation

1. **Clone the repository** (or download the script):
```bash
git clone https://github.com/yourusername/web-scraping-analyzer.git
cd web-scraping-analyzer
```

2. **Install required libraries**:
```bash
pip install requests beautifulsoup4 pandas matplotlib seaborn wordcloud
```

---

## Usage

1. Place your dataset (CSV) in the project folder.
2. Set the dataset path in the script:
```python
dataset_path = "/path/to/your/data.csv"
```
3. Run the script:
```bash
python analyzer.py
```

---

## Output
- Printed dataset statistics in the console.
- Visualizations displayed in separate windows.
- Word cloud for textual data.
- Processed dataset saved as `processed_dataset.csv`.

---

##  Notes
- If `quote` and `author` columns are detected, it will run **QuoteAnalyzer**.
- Otherwise, **GenericAnalyzer** will be used.
- CSV file should be UTF-8 encoded.
- Large datasets may take longer to process and render visualizations.

---

## License
This project is licensed under the MIT License — you are free to use and modify it.

# Buddy Matching Using Fuzzy String Similarity

This project builds a simple yet effective buddy-matching system for onboarding programs. It pairs new hires with existing buddies based on their survey responses using fuzzy string matching algorithms to identify the most compatible pairings. This system was developed as part of an onboarding initiative at Indiana University.

## Objective

To streamline the onboarding experience by matching new hires with mentors (buddies) based on shared interests, preferences, and professional backgrounds using automated similarity scoring.

## Data Source

Two CSV files are used:
- `New_Hire.csv`: Contains survey responses of incoming hires
- `Buddy.csv`: Contains survey responses of available mentors

These files are originally extracted from an Excel file with multiple sheets.

## Methodology

- Columns are mapped manually between the new hire and buddy survey forms.
- Fuzzy string similarity (using RapidFuzz and FuzzyWuzzy) is applied to match fields like interests, preferred working styles, and professional goals.
- A custom scoring function aggregates similarity across multiple question pairs.
- For each new hire, the buddy with the highest score is selected.

## Key Features

- **Flexible Field Mapping**: Explicit control over which survey questions are used for matching
- **Robust Similarity Scoring**: Handles spelling variations and partial matches
- **One-to-One Pairing**: Ensures unique buddy-new hire matches
- **Downloadable Output**: Matched results are downloadable in `.csv` format

## Libraries Used

```python
pandas, numpy, rapidfuzz, fuzzywuzzy, openpyxl

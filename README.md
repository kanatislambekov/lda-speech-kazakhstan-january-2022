# Analyzing Government Response in Kazakhstan after the January Protests

This repository contains code and a paper that analyze **public officials’ discourse** and **President Tokayev’s speeches** following the **January 2022 protests in Kazakhstan**.

Core artifacts:
- `Public officials.ipynb` — analysis of public officials’ statements and responses.
- `tokaev_speeches.ipynb` — text mining and discourse analysis of Tokayev’s speeches.
- `Islambekov_Analyzing_Government_Response_the_Case_of_Kazakhstan_after_the_January_Protests.pdf` — written report.

## Research question

How did Kazakhstan’s government and public officials frame their response to the January 2022 protests, and what patterns emerge in Tokayev’s speeches compared to broader official discourse?

## Data

The notebooks analyze a corpus of:
- **Public officials’ statements** collected from news outlets and government portals.
- **Tokayev’s speeches** (2022–2023), scraped or compiled manually.

> Data files are not included in this repository due to copyright. To reproduce the analysis, prepare text datasets and place them under `data/`:
>
> - `data/public_officials.csv`
> - `data/tokaev_speeches.csv`

Each CSV should contain at least:
- `date` (YYYY-MM-DD)
- `speaker`
- `text`

## Methods

Implemented in the notebooks:
- Preprocessing: cleaning, tokenization, stopword removal, lemmatization.
- Exploratory analysis: frequency counts, keyword-in-context (KWIC), collocations.
- Topic modeling: Latent Dirichlet Allocation (LDA) with coherence evaluation.
- Sentiment analysis: lexicon-based sentiment scores and comparative trends.
- Comparative discourse: clustering and visualization of similarities between Tokayev’s speeches and statements of other officials.

## Repository structure

```
.
├─ Public officials.ipynb
├─ tokaev_speeches.ipynb
├─ Islambekov_Analyzing_Government_Response_the_Case_of_Kazakhstan_after_the_January_Protests.pdf
├─ data/                # ← place text datasets here (ignored by git)
├─ requirements.txt
└─ .gitignore
```

## Quick start

### 1) Environment
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

### 2) Add data
Place your text datasets in `data/` as described above.

### 3) Run analysis
```bash
jupyter lab
```
Open the notebooks and run all cells.

## Key findings (high level)

- Officials’ discourse emphasized stability, security, and unity more than socioeconomic grievances.
- Tokayev’s speeches display a stronger emphasis on legitimacy, reform promises, and consolidation of power.
- Topic modeling shows diverging focus: officials stress order and law enforcement, Tokayev balances this with reform-oriented language.
- Sentiment analysis reveals an overall negative polarity in the immediate aftermath, gradually shifting toward neutral/positive framing.

See the PDF for the detailed report, figures, and references.

## Troubleshooting

- FileNotFoundError: ensure `data/` contains the necessary CSVs.
- Stopwords not found: install NLTK stopwords (`nltk.download('stopwords')`).
- Inconsistent encodings: ensure input files are UTF-8 encoded.

## License

Code in this repository is released under the MIT License. Text datasets must respect copyright and source terms.

## Acknowledgments

This project builds on discourse analysis, text mining, and comparative political communication literature, with application to Kazakhstan’s January 2022 protests.

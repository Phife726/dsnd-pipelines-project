# Pipeline Project

This project builds an end-to-end machine learning pipeline to predict whether a customer recommends a clothing product using the `Recommended IND` target variable.

The workflow combines:
- numeric features (for example `Age`, `Positive Feedback Count`)
- categorical product metadata (for example division/department/class)
- free-text review content (`Review Text`) processed with NLP

The implementation is completed in `starter/starter.ipynb` using a scikit-learn `Pipeline` and `ColumnTransformer` to combine preprocessing and modeling in a reproducible workflow.

## Getting Started

These instructions help you run the project locally.

### Dependencies

Python packages are listed in `requirements.txt`:
- `scikit-learn`
- `pandas`
- `spacy`
- `notebook`

You also need the spaCy English model:
- `en_core_web_sm`

### Installation

```bash
git clone <repository_url>
cd dsnd-pipelines-project
python -m pip install -r requirements.txt
python -m spacy download en_core_web_sm
jupyter notebook starter/starter.ipynb
```

## Testing

This repository does not include an automated test suite. Validation is done in the notebook by:
- training the pipeline on the training split
- generating predictions on the test split
- reviewing model performance metrics and outputs in notebook cells

## Project Deliverables

The submission work is completed in `starter/starter.ipynb`:

1. Load and inspect the dataset from `starter/data/reviews.csv`.
2. Define features (`X`) and target (`y = Recommended IND`).
3. Split data into training and test sets.
4. Perform exploratory data analysis (distributions, missing values, class balance).
5. Build preprocessing pipelines for numeric, categorical, and text columns.
6. Combine preprocessing with a classifier in a single scikit-learn pipeline.
7. Train, evaluate, and iterate on the model.

## Built With

- [scikit-learn](https://scikit-learn.org/stable/) - ML pipeline construction, preprocessing, and modeling
- [pandas](https://pandas.pydata.org/) - Data loading and analysis
- [spaCy](https://spacy.io/) - NLP tokenization/lemmatization for review text
- [Jupyter Notebook](https://jupyter.org/) - Interactive development environment

## License

[License](LICENSE.txt)

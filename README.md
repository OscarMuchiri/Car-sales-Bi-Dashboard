# Car Sales Business Intelligence Dashboard

A Power BI business-intelligence project for exploring vehicle-sales data and preparing decision-ready insights for areas such as inventory planning, customer segmentation, and targeted marketing.

The repository contains the original Power BI dashboard file together with a cleaned, reproducible Python notebook that documents the data-preparation workflow used before analysis.

---

## Project objective

The project is designed to turn a raw vehicle-sales dataset into a cleaner analytical dataset that can support dashboard reporting and business decision-making.

The source dataset used in the notebook contains:

- **157 vehicle records**
- **15 original columns**
- vehicle manufacturer and model information
- sales volume
- four-year resale value
- vehicle type
- price
- engine size and horsepower
- vehicle dimensions and curb weight
- fuel capacity and fuel efficiency
- latest launch date

---

## Repository structure

```text
Car-sales-Bi-Dashboard/
├── data/
│   └── README.md
├── notebooks/
│   └── car_sales_data_preparation.ipynb
├── .gitignore
├── LICENSE
├── README.md
├── car_sales_dashboard.pbix
└── requirements.txt
```

---

## Power BI dashboard

The original Power BI project is included as:

```text
car_sales_dashboard.pbix
```

Open the file in Microsoft Power BI Desktop to inspect and interact with the report.

The dashboard is the presentation layer of the project, while the notebook documents the data-cleaning logic separately for transparency and reproducibility.

---

## Data preparation workflow

The cleaned notebook preserves the core preparation steps from the original analysis.

### 1. Load the source dataset

The notebook expects:

```text
data/Car_sales.csv
```

### 2. Standardize missing-value placeholders

The following placeholders are converted to missing values:

```text
.
NA
N/A
na
```

### 3. Convert analytical fields to numeric types

The workflow converts these columns to numeric values:

- 4-year resale value
- Price in thousands
- Engine size
- Horsepower
- Wheelbase
- Width
- Length
- Curb weight
- Fuel capacity
- Fuel efficiency

### 4. Handle missing numeric values

Missing values in the numeric fields are filled using the **median of the corresponding column**.

Median imputation was retained from the original project because it provides a simple and reproducible way to complete the dataset without allowing extreme values to dominate the replacement value.

### 5. Create price categories

A derived `Price Category` field groups vehicles into:

| Category | Price in thousands |
|---|---:|
| Low | up to 20 |
| Medium | above 20 to 35 |
| High | above 35 |

### 6. Export the cleaned dataset

The notebook can write the prepared table to:

```text
data/car_sales_cleaned.csv
```

which can then be loaded into Power BI.

---

## Running the notebook

Create a Python environment and install:

```bash
python -m pip install -r requirements.txt
```

Place the source file at:

```text
data/Car_sales.csv
```

Then open:

```text
notebooks/car_sales_data_preparation.ipynb
```

and run the cells in order.

---

## Dataset note

The raw CSV is not redistributed in this repository because the original dataset source and redistribution terms have not yet been documented.

See [data/README.md](data/README.md) for the expected schema.

---

## Skills demonstrated

This project demonstrates:

- Power BI dashboard development
- business-intelligence reporting
- Python data cleaning
- pandas and NumPy
- missing-value treatment
- feature engineering
- analytical dataset preparation
- translating data into business-oriented reporting

---

## Portfolio role

This project complements the machine-learning and computer-vision projects in the portfolio by demonstrating a different capability: **business intelligence and decision-support analytics**.

---

## Author

**Oscar Muchiri**

Computer Scientist | Machine Learning • Software Engineering • Geospatial Systems

# Dataset Setup

The data-preparation notebook expects the raw input file:

```text
data/Car_sales.csv
```

The raw dataset is not currently redistributed in this repository because its original source and redistribution terms have not yet been documented.

## Expected source schema

The original notebook loaded a dataset with **157 rows and 15 source columns**:

```text
Manufacturer
Model
Sales in thousands
4-year resale value
Vehicle type
Price in thousands
Engine size
Horsepower
Wheelbase
Width
Length
Curb weight
Fuel capacity
Fuel efficiency
Latest Launch
```

During preparation, the notebook adds:

```text
Price Category
```

## Reproducing the workflow

Once the original CSV is available:

1. Place it in this directory as `Car_sales.csv`.
2. Run `notebooks/car_sales_data_preparation.ipynb`.
3. The notebook can export `car_sales_cleaned.csv` back into this directory.

Before publishing the raw dataset, document its original source and confirm that redistribution is permitted.

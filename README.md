# Cars EDA + Linear Regression Project

**Minor Project** | Udeep Karmakar

Exploratory Data Analysis and price prediction on used car listings from the CarDekho dataset.

## Dataset
- Source: [CarDekho Used Car Data (Kaggle)](https://www.kaggle.com/datasets/manishkr1754/cardekho-used-car-data)
- 15,411 raw rows, 15,244 after removing 167 duplicates
- Features: brand, model, vehicle age, km driven, seller type, fuel type, transmission, mileage, engine, max power, seats, selling price

## What I Did
1. Cleaned the data: dropped the index column, checked nulls, removed duplicates, standardized text labels
2. EDA with 6 charts: price distribution, top brands, price by transmission, km driven vs price, correlation heatmap, price by fuel type
3. Capped extreme price and km values at the 99th percentile
4. One-hot encoded fuel type, seller type and transmission type
5. Trained and compared two models (80/20 split)

## Model Results
| Model | R² Score | RMSE |
|---|---|---|
| Linear Regression | 0.743 | ~3.54 lakh |
| Random Forest Regressor | 0.936 | ~1.77 lakh |

## Key Findings
- Prices are heavily right-skewed, and most cars sell under ₹10 lakh
- max_power and engine size correlate most strongly with price
- Automatic cars have a higher median price than manual cars
- Price falls as vehicle age and kilometres driven increase

## Files
- `Udeep_Karmakar_Cars_EDA_Project.ipynb`: full notebook with outputs
- `Udeep_Karmakar_Cars_EDA_Project.pdf`: project report
- `cardekho_dataset.csv`: dataset

## Tools
Python, pandas, NumPy, matplotlib, seaborn, scikit-learn

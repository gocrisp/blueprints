# Groceries and essentials datasets

### DESCRIPTION
Groceries and essentials datasets from walmart, kroger, tesco, target and albertsons ... etc.

### SUMMARY
Get complete list of groceries and essentials datasets from walmart, albertsons, kroger, tesco .... etc

### SOURCE
https://data.world/crawlfeeds/groceries-and-essentials-datasets

### TRANSFORMATION
The dataset is transformed to Crisp like format.
```python
import pandas as pd
df = pd.read_csv('../datasets/albertsons/groceries_and_essentials_dataset_sample.csv')
df = df[['title', 'brand', 'primary_category', 'sub_category_1']]
df.rename(columns={'title': 'product', 'primary_category': 'product_category', 'sub_category_1': 'product_sub_category'}, inplace=True)
df.to_csv('../datasets/albertsons/groceries_and_essentials_dataset_sample_crisp_alike.csv', index=False)
```

### LICENSE
CC-BY-SA
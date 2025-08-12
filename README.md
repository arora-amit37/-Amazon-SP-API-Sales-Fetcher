# Amazon Orders Export Script

This Python snippet saves your `orders` data to a CSV file using **pandas**. If `orders` contains data, it will be exported to `amazon_orders.csv`. Otherwise, it will notify you that no data is available.

## Requirements

- Python 3.7+
- [pandas](https://pandas.pydata.org/)

Install dependencies:
```bash
pip install pandas
```

## Code Example

```python
import pandas as pd

if orders:
    df = pd.DataFrame(orders)
    df.to_csv("amazon_orders.csv", index=False)
    print(f"✅ Orders saved to amazon_orders.csv ({len(df)} rows).")
else:
    print("No data to save.")
```

## How It Works

1. Checks if the `orders` variable contains any data.
2. Converts the list of orders into a Pandas DataFrame.
3. Saves the DataFrame to `amazon_orders.csv` without the index column.
4. Prints a confirmation message showing the number of rows saved.
5. If no data is found, prints a "No data to save." message.

---

**Example Output:**
```text
✅ Orders saved to amazon_orders.csv (125 rows).
```
```text
No data to save.
```

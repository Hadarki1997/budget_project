# Budget Manager

A simple and clean Python project for managing and analyzing monthly expenses.  
The system loads data from an Excel file, cleans invalid entries, groups expenses by category, calculates statistics, and evaluates whether the user stays within the monthly budget limit.

---

## 🚀 Features

- Load expenses from an Excel (.xlsx) file  
- Clean and validate raw expense data  
- Calculate total spending  
- Calculate remaining budget  
- Generate category-based expense reports  
- Compute mean and median using NumPy  
- Check if the user is over the budget  
- Optional random month simulation  

---

## 📦 Requirements

Make sure you have the following packages installed:

```bash
pip install numpy openpyxl
```

---

## ▶️ How to Run

1. Run the script:
```bash
python summery.py
```

2. Enter your monthly budget limit:
```
Enter your monthly budget limit: 5000
```

3. Enter the name of the Excel file:
```
Enter Excel file name (including .xlsx): my_expenses.xlsx
```

4. The program will:
- Load all valid expenses  
- Print the full expense list  
- Show total spending  
- Display spending per category  
- Tell you whether you exceeded the budget  

---

## 📁 Excel File Format

The script expects the following columns:

- **Column C (index 2):** Category  
- **Column H (index 5):** Amount  
- **Column O (index 14):** Payment method  

Rows that contain totals or missing values are automatically skipped.

---

## 🧠 Main Components

### `clean_expenses()`
Cleans invalid expenses (empty category, non-positive amounts, etc.).

### `total_by_category()`
Returns a dictionary summarizing category totals.

### `categories_above()`
Finds categories whose total spending exceeds a threshold.

### `expense_stats()`
Returns (mean, median) using NumPy.

### `simulate_month()`
Generates random monthly expenses.

### `Budget` Class
Handles:
- Loading Excel data  
- Adding expenses  
- Calculating totals  
- Reporting categories  
- Checking budget limit  

---

## 📝 Example Output

```
===== EXPENSES LOADED =====
[{'category': 'Food', 'amount': 57.5, 'payment': 'Card'}, ...]

===== TOTAL SPENT =====
2287.83 ₪

===== CATEGORY REPORT =====
Food: 300.5₪
Rent: 2070₪
---------------------

===== BUDGET STATUS =====
You are within the budget.
```

---

## 👩‍💻 Author

Project by **Hadar giv**  
Python practice project for OOP, data cleaning, and Excel integration.


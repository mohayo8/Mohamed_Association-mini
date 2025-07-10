# Mohamed_Association-mini

# Association Rule Mining – Mini Assignment

**Objective:** Simulate transactional data and use association rule mining to discover shopping patterns.

---

## 🧰 Tools Used

- **Python** – for scripting and data simulation
- **pandas** – to structure and manipulate the dataset
- **mlxtend** – to run the Apriori algorithm and generate association rules

You can install required libraries using:
```bash
pip install pandas mlxtend


📜 What Each Code Cell Does
📌 Cell 1 – Simulate Transaction Data
Defines a list of 8 unique items (e.g., Bread, Milk, Eggs, Butter, etc.).

Simulates 10 random transactions.

Each transaction contains between 2 to 5 randomly selected items.

This models real-world shopping behavior for market basket analysis.

📌 Cell 2 – One-Hot Encode Transactions
Uses TransactionEncoder from the mlxtend.preprocessing module.

Transforms the list of transactions into a one-hot encoded format (True/False for each item per transaction).

Required preprocessing step for using the Apriori algorithm.

📌 Cell 3 – Find Frequent Itemsets
Applies the Apriori algorithm from mlxtend.frequent_patterns.

Sets the minimum support threshold to 0.3 (30%).

Finds all itemsets (combinations of items) that appear in at least 30% of the transactions.

Outputs the list of frequent itemsets.

📌 Cell 4 – Generate Association Rules
Uses association_rules() function from mlxtend.frequent_patterns.

Filters the rules by setting:

Metric: Confidence

Minimum threshold: 0.7 (70%)

Generates high-confidence rules based on the frequent itemsets.

Outputs key metrics for each rule, including:

Support – How often the itemset appears in the dataset

Confidence – How often the rule has been found to be true

Lift – How much more likely the consequent is, given the antecedent

# Association Rule Mining – Mini Assignment

## 📊 Rule Explanations

### ✅ Rule 1: {Butter} → {Cheese}
- **Confidence:** 1.00
- **Lift:** 1.67
- **Interpretation:** Every customer who bought Butter also bought Cheese. This strong rule suggests a reliable pattern — likely related to meal prep. A store could promote them together or use this pattern in product placement.

### ✅ Rule 2: {Bananas} → {Eggs}
- **Confidence:** 0.75
- **Lift:** 1.50
- **Interpretation:** Customers who buy Bananas often also buy Eggs — possibly for breakfast. This can help stores create promotions or design better shelf layouts.

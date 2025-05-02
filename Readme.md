# Titanic Survival Analysis

## Overview
This project explores the Titanic dataset to analyze survival rates based on gender. Using Python and data visualization libraries, we uncover insights into the survival patterns of passengers aboard the Titanic.

## Steps to Reproduce

### Step 1: Set Up Your Environment
1. Install [Anaconda](https://www.anaconda.com/) or ensure your Python setup is ready.
2. Install the required libraries by running:
    ```bash
    pip install pandas matplotlib seaborn
    ```

### Step 2: Load the Titanic Dataset
1. Open Jupyter Notebook.
2. Create a new Python notebook and name it `Titanic Survival Analysis`.
3. Load the dataset with the following code:
    ```python
    import seaborn as sns
    import matplotlib.pyplot as plt

    # Load Titanic dataset from seaborn
    df = sns.load_dataset('titanic')

    # Display first few rows to understand data
    df.head()
    ```

### Step 3: Analyze Survival Rates by Gender
Group the data by gender and calculate the average survival rate:
```python
# Group data by gender and calculate average survival rate
survival_by_gender = df.groupby('sex')['survived'].mean().reset_index()

# Display the result
print(survival_by_gender)
```

### Step 4: Visualize the Data
Create a bar chart to visualize survival rates by gender:
```python
# Create a bar plot to show survival rate by gender
sns.barplot(x='sex', y='survived', data=survival_by_gender)

# Add labels and title
plt.title('Survival Rate by Gender')
plt.ylabel('Survival Rate')
plt.xlabel('Gender')

# Show the plot
plt.show()
```

### Step 5: Write Observations
Example observation:
- "The survival rate for females was significantly higher than for males, with around 74% of women surviving compared to only 19% of men."

### Step 6: Save Your Work
1. Save your notebook as `titanic_survival_analysis.ipynb`.

## Key Takeaways
- Female passengers had a significantly higher survival rate compared to male passengers.
- Data visualization helps uncover meaningful insights from historical datasets.

## Tools Used
- Python
- Pandas
- Seaborn
- Matplotlib

## Repository
Find the project on GitHub: Your GitHub project link [here](https://github.com/MoizKhawar/titanic-survival-analysis)

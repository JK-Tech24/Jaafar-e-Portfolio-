<h1>Jaafar's e-Portfolio</h1>

<h2>About Me</h2>
<p>I am Jaafar, an Architect with a Master's degree in Project Management, currently pursuing a Master's degree in Artificial Intelligence. My work focuses on construction, engineering and infrastructure projects, with a particular focus on facility management and maintenance. I am committed to introducing AI solutions to create innovation, improve project productivity and increase environmental efficiency.</p>

<p><strong>Nationality:</strong> Lebanese / Canadian<br>
<strong>Birth Date:</strong> January 16, 1985</p>

<hr>

<h2>Professional Experience</h2>
<h3>Infrastructure Projects</h3>
<p>Managed and designed several large-scale infrastructure projects, ensuring quality and adherence to standards.</p>

<h3>Facility Management and Maintenance</h3>
<p>Currently working in facility management, overseeing day-to-day operations and maintenance.</p>

<hr>

<!-- Continue adding sections as needed -->

<h1>Jaafar's e-Portfolio</h1>

<h2>About Me</h2>
<p>I am Jaafar, an Architect with a Master's degree in Project Management, currently pursuing a Master's degree in Artificial Intelligence. My work focuses on construction, engineering and infrastructure projects, with a particular focus on facility management and maintenance. I am committed to introducing AI solutions to create innovation, improve project productivity and increase environmental efficiency.</p>

<p><strong>Nationality:</strong> Lebanese / Canadian<br>
<strong>Birth Date:</strong> January 16, 1985</p>

<hr>

<h2>Professional Experience</h2>
<h3>Infrastructure Projects</h3>
<p>Managed and designed several large-scale infrastructure projects, ensuring quality and adherence to standards.</p>

<h3>Facility Management and Maintenance</h3>
<p>Currently working in facility management, overseeing day-to-day operations and maintenance.</p>

<hr>

<!-- Continue adding sections as needed -->

<h2>Formative and e-Portfolio Activities (Machine Learning)</h2>

<h3>Seminar Preparation (Unit 2) - Undertaking Similar EDA with Auto-mpg Dataset</h3>

<details>
    <summary><strong>Identify Missing Values</strong></summary>
    In this step, I used the `isnull()` function from the Pandas library to check for any missing values in the dataset. By calling `.sum()` on the result, I obtained the total number of missing values for each column. This helped me understand the completeness of the data and identify any columns that might need attention or imputation.
</details>

<details>
    <summary><strong>Estimate Skewness and Kurtosis</strong></summary>
    I calculated the skewness and kurtosis of the dataset using the `skew()` and `kurtosis()` methods from Pandas. Skewness measures the asymmetry of the data distribution, while kurtosis indicates the "tailedness" of the distribution. These metrics provide insights into the nature of the data distributions, helping to assess normality and identify potential outliers.
</details>

<details>
    <summary><strong>Correlation Heat Map</strong></summary>
    To visualize the relationships between numeric variables, I created a correlation heat map using Seaborn and Matplotlib. First, I filtered the dataset to include only numeric columns and generated a correlation matrix. Then, I plotted the heat map, annotating it with the correlation coefficients. This visualization allowed me to easily identify strong correlations, which are valuable for understanding how different variables interact with each other.
</details>

<details>
    <summary><strong>Scatter Plot for Different Parameters</strong></summary>
    I created a scatter plot to examine the relationship between 'horsepower' and 'mpg' (miles per gallon). Using Seaborn's `scatterplot()` function, I was able to visually assess how changes in horsepower affected fuel efficiency. This type of visualization is essential for identifying trends and patterns in the data.
</details>

<details>
    <summary><strong>Replace Categorical Values with Numerical Values</strong></summary>
    To prepare the dataset for analysis, I converted the 'origin' categorical variable into numerical values using the `map()` function. This transformation is crucial for many statistical models that require numerical input. By mapping 'America' to 1, 'Europe' to 2, and 'Asia' to 3, I ensured that the data was suitable for further analysis. Finally, I printed the updated 'origin' column to verify the changes.
</details>

<details>
    <summary><strong>Python Code</strong></summary>
    <pre>
    ```python
    import pandas as pd
    import seaborn as sns
    import matplotlib.pyplot as plt

    # Load the dataset
    data = pd.read_csv("Unit02_auto-mpg.csv")  # Ensure the file name is correct

    # 1. Identify Missing Values
    missing_values = data.isnull().sum()
    print("Missing values per column:\n", missing_values)

    # 2. Estimate Skewness and Kurtosis
    skewness = data.skew()
    kurtosis = data.kurtosis()
    print("\nSkewness:\n", skewness)
    print("\nKurtosis:\n", kurtosis)

    # 3. Correlation Heat Map
    # Select only numeric columns for correlation
    numeric_data = data.select_dtypes(include=['number'])

    # Generate the correlation matrix
    correlation_matrix = numeric_data.corr()

    # Plot correlation heat map
    plt.figure(figsize=(10, 8))
    sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', linewidths=0.5)
    plt.title("Correlation Heat Map")
    plt.show()

    # 4. Scatter Plot for Different Parameters
    # Example: Scatter plot for 'horsepower' vs 'mpg'
    plt.figure(figsize=(8, 6))
    sns.scatterplot(data=data, x='horsepower', y='mpg')  # Adjust 'horsepower' and 'mpg' as needed
    plt.title("Horsepower vs MPG")
    plt.xlabel("Horsepower")
    plt.ylabel("Miles per Gallon (MPG)")
    plt.show()

    # 5. Replace Categorical Values with Numerical Values
    # Assuming 'origin' is a categorical column to convert
    data['origin'] = data['origin'].map({'America': 1, 'Europe': 2, 'Asia': 3})

    # Display the updated 'origin' column to verify changes
    print("\nUpdated 'origin' column:\n", data['origin'].head())
    ```
    </pre>
</details>

<h3>e-Portfolio Component (Unit 3) - Correlation and Regression</h3>

I ran the following four programs in my Jupyter Notebook. I modified variables where needed to observe how changes in data points impact correlation, regression, and predictions.

<details>
    <summary><strong>1. Covariance and Pearson Correlation</strong></summary>
    I used the `cov()` and `corr()` functions from Pandas to calculate the covariance and Pearson correlation between two variables. By changing the data values, I could observe how the relationship between the variables varied, reflected in the correlation coefficient and covariance.
</details>

<details>
    <summary><strong>2. Linear Regression</strong></summary>
    I applied linear regression using the `LinearRegression()` function from `sklearn`. I adjusted the dependent and independent variables (e.g., `Y` and `X`) to understand how changes in the dataset affect the model’s coefficients and predictions. I examined how modifying values in `Y` impacted the linear relationship.
</details>

<details>
    <summary><strong>3. Multiple Linear Regression</strong></summary>
    For multiple linear regression, I used the `LinearRegression()` model with multiple predictors (`X1`, `X2`, etc.). By modifying the input data, I explored how different predictors influence the target variable. I observed changes in the regression coefficients and the model’s ability to predict values based on multiple features.
</details>

<details>
    <summary><strong>4. Polynomial Regression</strong></summary>
    Polynomial regression was performed using the `PolynomialFeatures()` and `LinearRegression()` models. I modified the degree of the polynomial and the input values to observe the fit of the model. By increasing the polynomial degree or changing the input data, I observed how the model’s complexity and accuracy changed.
</details>

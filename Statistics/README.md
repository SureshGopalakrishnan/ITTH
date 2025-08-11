Sampling Techniques Assignment  
This Jupyter Notebook (SamplingTechniques.ipynb) contains two main sections that demonstrate different sampling techniques using the Pandas library in Python.

Simple Random Sampling for Flight Details  
This section focuses on creating a simple random sample from a dataset of flight details.

The data includes:
- Customer Name: A list of customer names.
- Seat Number(s): A list of seat numbers assigned to each customer.
- Number of Family Member(s): The count of family members for each customer.

The code creates a dictionary of this data, converts it into a Pandas DataFrame, and then uses the .sample() method to select a random sample of 5 rows from the DataFrame.

Stratified Sampling for Sports Person Data  
This section demonstrates how to perform stratified sampling on a dataset of sports person details, categorized by the type of award they received (e.g., Gold, Silver, Bronze).

The data includes:
- Person Name: A list of player names.
- Category: The award category (e.g., 'Gold', 'Silver', 'Bronze').
- Cash Award: The amount of the cash award received.

The code first creates a dictionary and converts it into a DataFrame. It then uses the groupby() method on the 'Category' column, followed by a lambda function that samples from each group. This ensures a representative sample from each category, even if some categories have a small number of entries.

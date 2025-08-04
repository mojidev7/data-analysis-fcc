CSV Using Pandas

    import pandas as pd
    df = pd.read_csv("myfolder/myfile.csv", parse_dates=["Date"])
    df.shape #(rows, columns)
    df.info() #info of the dataframe
    df.describe() #statisticate properties



Numerical Analysis

    df["Unit_Cost"].describe() #shows mean, max, std, count, 25%, 50%, 75%
    df["Unit_Cost"].mean() #shows meean
    df["Unit_Cost"].median() #shows 50%
    df["Age_Groups"].value_counts() #count different data (same as GROUP BY in SQL)


Create New Columns In DataFrame 

    df["a"] = df["b"] * 2 #a column is new
    sales['Calculated_Date'] = sales[['Year', 'Month', 'Day']].apply(lambda x: '{}-{}-{}'.format(x[0], x[1], x[2]), axis=1)



Selecting and Indexing

    df.loc(df["city"] == "Tehran") #can use or(|), and(&)
    df.loc(df["city"] == "Tehran", "Country") #after filter, select only country
    sales.loc[(sales['Country'] == 'Canada') | (sales['Country'] == 'France')].shape[0] #how many..




Plot Using Pandas

    sales["Customer_Age"].plot(kind='kde', figsize=(14, 5))
    sales['Customer_Age'].plot(kind='box', vert=False, figsize=(14,6))
    sales["Order_Quantity"].plot(kind='hist', bins=30, figsize=(14,6))
    sales["Year"].value_counts().plot(kind='pie', figsize=(6,6))
    sales["Month"].value_counts().plot(kind='bar', figsize=(12, 4))
    sales.plot(kind='scatter', x='Unit_Cost', y='Unit_Price', figsize=(6, 6))

    sales[["Profit", "Country"]].plot(kind='box', by='Country', figsize=(10, 4))
    sales[['Profit', 'Country']].boxplot(by='Country', figsize=(10,6))



Date Usage Using Pandas

    sales['Calculated_Date'] = sales[['Year', 'Month', 'Day']].apply(lambda x: '{}-{}-{}'.format(x[0], x[1], x[2]), axis=1)
    sales['Calculated_Date'] = pd.to_datetime(sales['Calculated_Date'])


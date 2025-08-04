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



Selecting and Indexing

    df.loc(df["city"] == "Tehran") #can use or(|), and(&)
    df.loc(df["city"] == "Tehran", "Country") #after filter, select only country


Plot Using Pandas

    sales["Customer_Age"].plot(kind='kde', figsize=(14, 5))
    sales['Customer_Age'].plot(kind='box', vert=False, figsize=(14,6))

Rossmann Store Sales Prediction

This project aims to predict daily sales for Rossmann drug stores using machine learning techniques. Accurate sales forecasts enable store managers to create effective staff schedules, enhancing productivity and customer satisfaction.
Description

Rossmann operates over 3,000 drug stores in 7 European countries. The challenge is to predict 6 weeks of daily sales for 1,115 stores located across Germany. Factors influencing sales include promotions, competition, holidays, seasonality, and locality. This project builds a robust prediction model to aid store managers.
Evaluation

Submissions are evaluated using the Root Mean Square Percentage Error (RMSPE):
RMSPE=1n∑i=1n(yi−y^iyi)2RMSPE=n1​∑i=1n​(yi​yi​−y^​i​​)2

​
where yiyi​ is the actual sales and y^iy^​i​ is the predicted sales. Days and stores with 0 sales are ignored in scoring.
Data

Historical sales data for 1,115 Rossmann stores is provided. The task is to forecast the "Sales" column for the test set.
Files

    train.csv - Historical data including Sales
    test.csv - Historical data excluding Sales
    sample_submission.csv - Sample submission file in the correct format
    store.csv - Supplemental information about the stores

Data Fields

    Id: Represents a (Store, Date) duple within the test set
    Store: Unique Id for each store
    Sales: Turnover for a given day (target variable)
    Customers: Number of customers on a given day
    Open: Indicator if the store was open (0 = closed, 1 = open)
    StateHoliday: Indicates a state holiday (a = public holiday, b = Easter holiday, c = Christmas, 0 = None)
    SchoolHoliday: Indicates if the store was affected by school closures
    StoreType: Differentiates between 4 store models (a, b, c, d)
    Assortment: Assortment level (a = basic, b = extra, c = extended)
    CompetitionDistance: Distance to the nearest competitor store
    CompetitionOpenSince[Month/Year]: Year and month when the nearest competitor opened
    Promo: Indicates if a store is running a promo on that day
    Promo2: Continuing promotion for some stores (0 = not participating, 1 = participating)
    Promo2Since[Year/Week]: Year and week when Promo2 started
    PromoInterval: Months when Promo2 starts anew (e.g., "Feb,May,Aug,Nov")

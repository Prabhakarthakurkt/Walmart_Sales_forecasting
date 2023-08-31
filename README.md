# Walmart_Sales_forecasting
In this project, student are provides with historical sales data for 45 waltmart stores located in different regions.
Each store contain many departments, and participants must project the sales for each store. to add to the challenge, selected holiday markdown events are include in the dataset. these markdowns as known to effect sales, but it is challenging which departments are affected and the exttent of the impact.
you may only use the provided data to make your predictions.
# Data

you are provided with historical sales data for 45 walmart stores located in different regions. Each store contains a number of dapartments, and you are tasked with predicting the department-wide sales for each store.

in addition, walmart runs serverl promotional markdown events throughtout the year. These markdowns precede prominent holidays, the four largest of which are the super bowl , labor day ,Thanksgiving, and christmas . the weeks including these holidays are weighted five times higher in the evaluation than non-holiday weeks. part of the challenge presented by this competition is modeling the effects of markdowns on these holiday weeks in the absence of complete/idea  historical data.
 the  basic idea of analyzing the walmart forcasting dataset is to get a fair idea about the factors affecting the sales of the walmart store.

 # Problem Statement 

   By using these data we have to predict the walmart sales forcasting based on different parameters


# Data Desctiption 

    stores.cvs

    this file contains anonymized about the 45 stores, indicating the type and size of store.


    train.cvs 

    this is the historical training data, which covers to 2010-11-02 to 203-01-01 . which this file you will find the following fields.

    store -  the store number 
    dept -   the department number 
    date - the week 
    weekly_sales - sales for the given department in the given store
    IsHoliday - whether the week  is a special holiday week 
    test.csv

this file is identical to train.csv except we have withheld the weekly sales. you must predict the sales for each triple of store, department, and date in this file.

feature.csv 

this file contains additional data releted to the store, department, and regional activity for the given dates . it contains the following field:

    store - the store number 
    Date - the week 
    Temperature - average temperature in the region
    fuel_price -cost of fuel in the region 
    MarkDown1-5  - anonymized data related to promotional markdown that waltmart is runing, martdown data is only available after Now 2011, and is not available for all stores all the time, any missing value is marked with an NA.
    CPI - The consumer price index 
    Unemployment - the unemployment rate
    IsHoliday - whater the week is a special holiday week 


For convenience, the four holiday fall within the follwing weeks in dataset(not all holidays are in the data):


## Business objectives and constraints

  1. The cost of a mis-classification can be very high .
  2. There is some latency concerns.
  
### this is formatted as code


# imoprting Libraries


    import numpy as np
    import pandas as pd

    import matplotlib.pyplot as plt
    import matplotlib.patches as patches 
    import seaborn as sns 
    import plotly.express as px
    import plotly.graph_obj as go 
    import plotly.offline import iplot

    from sklearn.model_selection import train_test_split
    from math import sqrt 
    from sklearn.model import Ridge
    from sklearn.linean_model import Lasso
    from sklearn.metrics import mean_squared_error as mse
    from sklearn.metrics import r2_score
    from sklearn.model_selection  import GridSearchcv
    from sklearn.model_selection improt Randomizedsearchcv
    import warnings

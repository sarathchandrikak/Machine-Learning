# Time Series Prediction / Forecasting 

#### Intro

Any data that has a time component involved in it is termed as a time-series data. 
An archaeological record of human occupancy at a single locality during a specific period of time

    Quantitative Forecasting - Based on the data and any repeating historical patterns in the data
    Captures complex patterns which human cannot identify. Quantitative forecasting is made when data is available and no experts are required.
    No bias  Eg: Time Series Forecasting
    
    
    Qualitative Forecasting - Procedure is taken when data is not available and historical patterns do not repeat. This is based on an expert 's decision. 
    May not capture complex patterns. 
    Bias, Eg: Delphi method

#### Basic Steps for forecasting

      -> Define the problem and convert to time series analysis problem 
      -> Collect data
      -> Analyze the data
      -> Gives us different structures and patterns in the data
      -> Data treatment before using for modeling
      -> Build and evaluate forecast model
      -> Understand the business objective, identify the 1 or 2 models
      -> Which is best	
      -> Which forecast is accurate and least error
      -> What is the complexity of the model and usability



#### Questions to consider while solving

1. Define the problem
         
       -> What quantity are you forecasting -> Is it price, number of units, profit / revenue
       -> What level of granularity -> are we doing it at a store level, region level, country level
       -> What frequency are you generating -> Every month, year, week

2. Forecast Horizon

       -> Short term -> For Small goals Eg: How to schedule workforce, machines
       -> Medium term -> For Target setting Eg: Number of people hiring for company
       -> Long term forecast -> For Strategic decisions. Eg: Whether to start a new branch in a new location. 

Example: 
    Quantity -> No. of units sold
    Granularity -> Region (50 - 100 stores)
    Frequency -> Monthly
    Horizon -> Medium term or quarterly

#### Forecasting Approaches

##### Model Building Approaches

1. Top down approach - Forecast monthly sales of company and breakdown region wise and month wise. 
2. Bottom up approach - We start with the most granular level. Data at a store level. Aggregate at region level

##### Rules to consider while defining the problem

    1. The Granularity Rule: 
          The more aggregate your forecasts, the more accurate you are in your predictions.
          Try to define a good granular levels
    
    2. The Frequency Rule:
          Keep updating forecasts regularly to capture new information that comes. 
          Based on external situations or other factors adjust frequency.

    3. The Horizon Rule:
          When we have the horizon planned for a large number of months into the future, we are more likely to be accurate in the earlier months as compared to the later ones. 
          The farther ahead we go into the future, the more uncertain we are about the forecasts. 

#### Analyze the data: 

Components of time series data:
          
      Level -> Baseline of a time series. This gives the baseline to which we add the different other components. 
      Trend -> Over a long term, an indication of whether the time series moves lower or higher. 
      Seasonality -> Repeatable patterns in the data in fixed period. 
      Cyclicity -> It doesn't have to be periodic. The intervals between cycles can’t be fixed. 



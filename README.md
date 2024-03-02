# Google-Fiber-Project
### Google Fiber: What happens after the first call?  
This project recounts the behavior of customers on their first call and after it.  
# [Link to the dashboard: public.tableau](https://public.tableau.com/views/GoogleFiberCase/WHY_1?:language=es-ES&:sid=&:display_count=n&:origin=viz_share_link)

## Problem and context:
Google Fiber is Google's technical service, a call center. Where we want to know the behavior of the customers who call, to know which are the most recurring problems and whether after the first call these problems decrease or not. With the purpose of improving its effectiveness.

## Databases:
For this, three databases were delivered (three .CSV files), one from each different market (market_1, market_2, market_3).

## EDA: Exploratory Data Analysis
These data were collected in the first quarter of the year (January, February and March) and contain the number of calls that arrived per day. Where they present which ones are calling for the first time (contacts_n) and which ones are calling after a day has passed since their first call (contacts_n_1), up to 7 (contacts_n_7). Where your type of problem is specified (type_1 to 5).
#### The types of problem would be:
- Type_1: account management
- Type_2: technical troubleshooting
- Type_3: scheduling
- Type_4: construction
- Type_5: internet and wifi

## Transformations
These three databases were loaded into BigQuery and transformed to form a single database, which contained the three markets and had a better understanding. Leaving something like the following:

## Analysis and Visualization:
The above database was loaded into Tableau where it was divided into three different dashboards:
### 1) When and how many do they call?
For when they showed up on what day of the week, clients generally call, divided into three by month. It was observed that customers call much less on weekends.
For how many call, the number of calls is presented for the different "contacts_n" and for months. Where in general the calls decrease as the days go by, the first call being the day in which they call the most with a big difference.

### 2) Why are they calling?
This dashboard presents the distribution of problems for each market by month. In two bar graphs, where one is given by the first call (contacts_n) and the other by one day after the first call (contacts_n_1), which is where the change was observed the most.  
Here we observe that market_1 and market_2 behave in a similar way, while market_3 is quite different. Where for market_1 and 2 the problems of type_2 and type_5 are the most common and after a day the type_5 increases by a certain amount (more for market_1), on the other hand for market_3 the most common problem by far is type_5 followed by type_2 but with a greater difference, and after one day the % of problems for type_5 remains the same and that of type_2 decreases, which causes an increase in type_1

### 3) All data
This dashboard presents two tables, one has the types of problems by market and contacts_n. While the other presents the number of calls for each day of the three months.

## Conclusion:
- The most common problem is due to type_ 2 and type_5, which would be technical problems and Internet and Wi-Fi, respectively.
- Users usually call more from Monday to Friday.
- In March there was a significant increase in first calls (3K).
- Market_3 works better with type_2 problems than the other two.

## Next Steps:
- Collect data for one year, to have a better database to view.
- Take into account the number of calls per market, that is, which market is receiving the most calls? Do they persist throughout the days?

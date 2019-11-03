# Deployed Shiny App
[Sales Dashboard App](https://charlehl.shinyapps.io/sales_dashboard_forecast_app/)

# Summary:
Learning Shiny Web App development from Business Science University Course

Learned how to create a dashboard using Flexdashboard and integrating Shiny for UI reactivity.  The dashboard 
allows the user to see bike sales based upon bike type and family selected within a selected date range.  A Choropleth map to denote sales based 
upon the user selected input is shown.  In addition, a line chart is shown denoting the sales based upon the user input.  The user is allowed to drill 
down into the chart further based upon daily, weekly, monthly, quarterly and yearly sales aggregation. Additionally, the user can also forecast sales 
using an XGBoost or linear regression model dependent upon the time scale chosen.  The application will dynamically make predictions based upon the inputs 
selected on the dashboard as well as the time unit.  Learned how to customize apps using CSS.

Also learned how to create a price prediction app using a Xgboost trained model.  The app also uses 
Shiny for UI reactivty allowing the user to input a bike name, family and type and to then predict the 
price and to also plot the bike on a plot of established bike products.

Apps shown are the output from course material.  Currently, working on an independent app based upon the knowledge learned during the course.  App will 
be a dashboard looking at the educational expenditures by state in the US and looking at the testing performance.

# Implementation Notes for Project

### App was deployed using shinyapps.io
# Summary:
Learning Shiny Web App development in Business Science University Course

Learned how to create a dashboard using Flexdashboard and integrating Shiny for UI reactivity.  The dashboard 
allows the user to see bike sales based upon bike type and family selected within a selected date range.  A Choropleth map to denote sales based 
upon the user selected input is shown.  In addition, a line chart is shown denoting the sales based upon the user input.  The user is allowed to drill 
down into the chart further based upon daily, weekly, monthly, quarterly and yearly sales aggregation. 

Also learned how to create a price prediction app using a Xgboost trained model.  The app also uses 
Shiny for UI reactivty allowing the user to input a bike name, family and type and to then predict the 
price and to also plot the bike on a plot of established bike products.  Further learned how to add CSS for 
styling of web app.

# Implementation Notes for Project


## Reactive Filtering from Dashboard Inputs
Apply button for dashboard with ignoreNULL defined to allow initial startup of dashboard

```r
process_data_filter_tbl <- eventReactive(
  eventExpr = input$apply, 
  
  valueExpr = {
  
  processed_data_tbl %>%
    
    filter(order.date %>% between(left  = input$date_range[1], 
                                  right = input$date_range[2])) %>%
    filter(category_1 %in% input$checkbox_category_1) %>%
    
    filter(category_2 %in% input$picker_category_2)},
  ignoreNULL = FALSE
)
```

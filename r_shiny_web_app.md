# Summary:
Learning Shiny Web App development in Business Science University Course

# Implementation Notes for Project


## Reactive Filtering
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

## Creating reactive filtering from dashboard inputs
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
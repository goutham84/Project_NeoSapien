Project Overview
This repository contains a Python-based performance analysis dashboard for analyzing app logs. The goal of the project is to extract meaningful insights from the logs, visualize app health metrics, and implement basic anomaly detection to identify performance issues.

**Dataset**
The dataset includes 7 days of app logs with the following fields:

  **timestamp:** Time of the request
  
  **endpoint:** API endpoint called
  
  **response_time_ms:** Response time in milliseconds
  
  **status_code:** HTTP status code
  
  **user_id:** Anonymous user identifier
  
  The dataset is provided as a CSV file.


**Approach**

**1. Data Loading and Preprocessing**
    The dataset is loaded and parsed from the provided file.
    The timestamp column is converted to datetime format for time-based analysis.

    
**2. Performance Metrics Calculation**:
    Key metrics were computed to evaluate app performance:
    
    Average and P95 Response Times: Calculated for each API endpoint.
    Error Rates: Percentage of non-200 HTTP status codes.
    Slow Requests Percentage: Proportion of requests taking more than 1 second.
    Peak Usage Periods: Hourly distribution of request counts.
    
**3. Visualization Dashboard**
    Visualizations were created to make the insights actionable:
    
    Response Time Trends: Time-series trends of response times by endpoint.
    Error Rate Patterns: Bar chart showing error rates for each endpoint.
    Endpoint Performance Comparison: Comparison of average and P95 response times.
    Peak Usage Periods: Hourly request counts plotted over time.
    
**4. Anomaly Detection**
      Anomalies were identified to flag potential issues:
          Response Time Anomalies: Based on z-scores of response times.
          Error Rate Anomalies: Using standard deviation thresholds.
          Endpoint Availability Issues: Identifying periods with zero requests.
          
**5. Code Quality and Testing**
      Functions include error handling for robustness.
      Key functions are unit tested to ensure correctness.
      Key Insights
      Response Time: Certain endpoints exhibited high average and P95 response times, indicating potential bottlenecks.
      Error Rates: Specific endpoints had significantly higher error rates, requiring further investigation.
      Peak Usage: High traffic was observed during certain hours, revealing critical usage periods for scaling.
      Anomalies: Detected unusual spikes in response times and endpoints with availability issues.
      
**Future Improvements**
    Incorporate more advanced anomaly detection techniques like machine learning models.
    Add interactivity to the dashboard (e.g., using libraries like Plotly or Dash).
    Expand metrics to include user-level insights or additional app health KPIs.

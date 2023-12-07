---
title: Dashboards
Purpose: This doc will provide general information about the summary dashboard, custom reports. 
---


## Summary dashboard

For greater insights into your service usage, access the dedicated {% konnect_icon analytics %} [Analytics](https://cloud.konghq.com/analytics) page.

From {% konnect_icon analytics %} Analytics, you can view dashboards, access historical data for a range greater than 30 days, and customize the entities in a report:
* View the Analytics summary dashboard to track traffic, errors by error code, and latency across all services in your organization.
* [Export historical data in CSV format](#export-analytics-data) for any individual service.
* [Create a custom report](/konnect/analytics/generate-reports/) for any number of services, routes, or applications, filtered by time frame and grouped by metric.

The summary dashboard provides metrics across all services in your organization within a selected time interval for the following categories:

* **Traffic**
* **Errors**
* **Latency**

These categories measure trends by comparing metrics across fixed comparable time intervals and plotting the data points. For example, hour-over-hour, day-over-day, week-over-week, and month-over-month.
You can view a graph for each category by clicking **Traffic**, **Errors**, or **Latency**, and switching between the views.

* **Traffic**: This graph displays the total number of HTTP requests categorized by successful and failed requests over the specified time interval.
    * Successful requests contain all requests that returned a **1xx-3xx** status code.
    * Failed requests contain all requests that returned a **4xx-5xx** status code.
    * 6xx status codes are not reported.

    ![traffic analytics graph](/assets/images/products/konnect/analytics/konnect-vitals-traffic.png){:.image-border}
    > _**Figure 2:** Graph showing successful and failed requests over the past three hours._

* **Errors**: This graph displays the total number of failed HTTP requests categorized by error response codes over the specified time interval. Error response codes include any **4xx-5xx** status codes.

    ![errors analytics graph](/assets/images/products/konnect/analytics/konnect-vitals-errors.png){:.image-border}
    > _**Figure 3:** Graph showing errors by 4xx and 5xx error codes received over the past three hours._

* **Latency**: This graph displays request latency, in milliseconds, of the 99th, 95th, and 50th percentiles.
Admins can monitor the latency, investigate where delays are noticed, and optimize performance for APIs.

    {:.note}
    > **Note**: Latency data is only available for requests proxied through a data plane running {{site.base_gateway}} 3.0.0.0 or later.

   ![latency analytics graph](/assets/images/products/konnect/analytics/konnect-analytics-latency.png){:.image-border}
  > _**Figure 4:** Graph showing latency as a percentage over the past 15 minutes._

Graphs can be interacted with, including hovering over chart items to display more details, and filtering options by clicking on items in the **legend**.

You can select a time period using the **time period** drop-down menu. The intervals aggregate data at different increments of time.


## Contextual analytics for services and routes

In the [Gateway Manager](/konnect/gateway-manager/), you can see
activity graphs for gateway services or routes for the past 30 days.
For gateway services and routes, the graphs show requests broken down by status codes.


![service graph](/assets/images/products/konnect/analytics/konnect-analytics-gateway-service.png){:.image-border}

> _**Figure 1:** Graph showing traffic for the last 15 minutes by status code for a gateway service._


You can also [export historical data in CSV](#export-analytics-data) format from any graph.
# Capacity Planning of Oracle Databases

## Introduction

In this lab, you will go through the steps to explore Capacity Planning for Oracle Databases.

Estimated Time: 15 minutes

### Objectives

-   Explore Capacity Planning for Oracle Databases.

### Prerequisites

This lab assumes you have completed the following labs:
* Lab: Enable Demo Mode

## Task 1: Capacity Planning - Databases

1.  On the **Operations Insights Overview** page, from the left pane click on **Capacity Planning**.

      ![Left Pane](./images/capacity-planning-ocw.png " ")

2.  On the **Database Capacity Planning** page, you will obtain a fleet-wide overview of your resource consumption and trends.  CPU insights, storage insights, and memory insights give a quick view into top resource consumers now and forecast potential resource bottlenecks over the selected period.

      ![Left Pane](./images/database-capacity-planning-ocw.png " ")

    From this page you can perform the following tasks in support of the Capacity Planning use case goals:

    * View total allocation and utilization of CPU, Storage, Memory, and I/O resources for all (enabled) databases in the compartment
    * Identify top-5 databases of CPU, Storage, and Memory by absolute usage or utilization percentage
    * Identify top-5 databases by CPU, Storage, and Memory growth over the period
    * See aggregated historical usage trends for CPU, Storage, and Memory over the period

3.  From **Time Range** on the left pane select **Last 90 days**.

      ![Left Pane](./images/time-range-ocw.png " ")

4.  Review the **Inventory** section. The **Inventory** section displays the total number of databases enabled for Operations Insights along with the database types. In addition, the CPU, Storage, Memory, and I/O usage charts display overall resource consumption (Top Consumers and UsageTrend) by these database targets.

      ![Left Pane](./images/inventory-ocw.png " ")

5.  **CPU Insights** - Database utilization percentage for the 90th percentile value of the daily average CPU Usage over the selected time period. These sections show the number of databases running with low (0–25%) and high (75–100%) utilization of CPU.

      ![Left Pane](./images/cpu-insights-ocw.png " ")

6.  **Storage Insights** - Database utilization percentage for the 90th percentile value of the daily average Storage Usage over the selected time period.  These sections show the number of databases running with low (0–25%) and high (75–100%) utilization of storage.

      ![Left Pane](./images/storage-insights-ocw.png " ")

7.  **Memory Insights** - Database utilization percentage for the 90th percentile value of the daily average Memory Usage over the selected time period.  These sections show the number of databases running with low (0–25%) and high (75–100%) utilization of memory.

      ![Left Pane](./images/memory-insights-ocw.png " ")

## Task 2: Capacity Planning - CPU

1.  On the **Database Capacity Planning** page, from the left pane click on **CPU**.

      ![Left Pane](./images/database-cpu-ocw.png " ")

2.  **Database CPU** page has a master-detail design with three primary components:

    * Insights – table of databases flagged for CPU utilization insights
    * Aggregate – treemap of CPU utilization over all databases in the compartment
    * Trend & Forecast – time series charts of CPU usage trends and forecasts for individual or groups of databases

      ![Left Pane](./images/database-cpu1-ocw.png " ")

3.  On the **Database CPU** page, under **Insights** tab, select **30 Day High Utilization Forecast** against **Databases**, to view database CPU utilization forecast for next 30 days.

      ![Left Pane](./images/utilization-forecast.png " ")

4.  Under the **Database Display Name** column, select the row corresponding to the **CRM-ST** database.

      ![Left Pane](./images/crm-st-database-ocw.png " ")

5.  Check the **Utilization (%)** and **Usage Change (%)** for database **CRM-ST**.
    
    * Utilization (%) -  Utilization percentage for the 90th percentile value of the daily average storage usage over the selected time period
    * Usage Change (%): Percentage change in the linear trend of storage usage over the selected time

6.  The **Trend and Forecast** chart displays historical time series plots related to CPU allocation and usage for the selected database **CRM-ST**.

      ![Left Pane](./images/trend-and-forecast-ocw.png " ")

7.  Historical CPU Usage (dark solid green line) is the Avg Usage - average value of daily (hourly) CPU usage data

8.  Avg Usage Forecast - forecast of Avg Usage data using linear forecast model (Dashed Green line) and the Max Allocation - maximum allocation of CPU for the database.

9.  The value **56.42** AVG ACTIVE CPU USAGE is forecasted for after 15 days for Avg usage of CPU.

10.  Select **Max Usage** from the legend on the right side. The red line is **Max Usage** - maximum value of daily (hourly) CPU usage data for database **CRM-ST**.

      ![Left Pane](./images/max-usage-cpu-ocw.png " ")

11.  Select **Max Usage Forecast** from the legend on the right side.

      ![Left Pane](./images/max-usage-forecast-ocw.png " ")

12.  The value **77.07** AVG ACTIVE CPU USAGE is forecasted for after 15 days for Max usage of CPU.

    You can see the difference in average forecasted value v/s Max forecasted value. If the workload is critical and cannot tolerate any performance issues then the database must be allocated the max forecasted value. If the workload is not so critical and can tolerate deviations in performance then it is ok to allocate CPU based on average forecasted value and save money.

13.  The trending and forecast chart facilitates:

     * Forecast future maximum and average demand for CPU resources
     * Compare current usage to allocation to detect over-provisioning
     * Compare maximum to average usage and trends to assess demand volatility
     * Forecast difference between the maximum and average daily CPU usage to estimate potential savings from workload smoothing

14.  Click **Aggregate** on the top and from **Grouping** select **Database Type**.

      ![Left Pane](./images/aggregate-database-ocw.png " ")

     The page displays a Treemap of all databases breaking it down by Database Type. This lets you compare how your different, individual databases are using their resources as well as between various database types. This also lets you review the problem across fleet of databases. The databases with dark color are critical and are high on utilization. The size of the box displayed on the treemap shows usage in terms of active CPU.

## Task 3: Capacity Planning - Storage

1.  Click on the **Storage** menu on the left panel.

      ![Left Pane](./images/storage-menu-ocw.png " ")

2.  You get a complete view of storage usage across all Operations Insights enabled databases

      ![Left Pane](./images/database-storage-ocw.png " ")

    From here we can identify servers with underused or overused storage and also compare storage utilization between databases.

3.  From the drop-down on the top select **30 Days High Utilization Forecast**.

      ![Left Pane](./images/storage-utilization-forecast-ocw.png " ")

4.  In the **Trend & Forecast** chart View the storage trend and usage forecast for the selected database.

      ![Left Pane](./images/storage-trend-forecast-ocw.png " ")

5.  In the **Trend & Forecast** chart View click on **Machine Learning** to project future resource consumption. Machine Learning is a more advanced model that considers seasonality.

      ![Left Pane](./images/storage-trend-forecast-ml-ocw.png " ")

6.  From the drop-down on the top select **All** and search for **PAYD** database. Select **PAYD** database.

      ![Left Pane](./images/storage-menu-payd-ocw.png " ")

7.  In the **Trend & Forecast** chart View the storage trend and forecast for the selected database.

      ![Left Pane](./images/storage-trend-payd.png " ")

8.  Select **Max usage** and **Max usage forecast** from the right panel.

      ![Left Pane](./images/storage-trend-max-payd.png " ")

      You can see the average forecasted value v/s Max forecasted value for storage. **Max Usage Forecast** for this database is 0.2 TB, whereas **Allocation** shows that total storage allocated to this database is 4 TB. Since, allocation is more but storage used or forecasted is less, it is ok release some storage for this database and save money on storage.



## Acknowledgements

- **Author** - Vivek Verma, Master Principal Cloud Architect, North America Cloud Engineering
- **Contributors** - Vivek Verma, Sriram Vrinda, Derik Harlow
- **Last Updated By/Date** - Vivek Verma, May 2022
# A-Simulation-Analysis-using-JaamSim
Optimizing Customer Experience at  Z Beans Coffee Shop: A Simulation Analysis using JaamSim

![image](https://user-images.githubusercontent.com/80241823/221757044-6bacd72a-ab67-4678-bf41-8a2cabfd7e69.png)

## 1. Executive Summary 

This report provides a detailed analysis of customer behavior at Z Beans Coffee Shop on the Mercer University campus in Atlanta, focusing on optimizing business operations to enhance customer experience. Z Beans has experienced challenges managing customer flow and providing efficient service during peak hours, negatively impacting its reputation and customer loyalty. First, we analyzed the data we collected using Python and Excel to determine appropriate distributions for arrival, service time for orders, food pick-up, and dwell time. Then we utilized JaamSim software to model and analyze customer behavior based on our findings to provide recommendations for improvement.
Sensitivity analysis was conducted by collecting data on input variables such as throughput, interarrival time, waiting queues, and dwell time and analyzing their impact on the coffee shop's operations. The study identified potential bottlenecks and areas for improvement, including increasing staffing levels during peak hours, table turnover, and the number of servers to improve customer flow and satisfaction.
The report highlights the origin story of Z Beans Coffee Shop, founded in 2016 by former Mercer graduate student Shane Buerster, who traveled to Ecuador to find an alternative to gold mining and started the business to promote fair and direct trade of Ecuadorian coffee. Knowing the origin story of Z Beans Coffee Shop can help to build customer loyalty, differentiate the business from competitors, and provide context for its success.
In addition, the study provides valuable insights into customer behavior and recommendations for enhancing business operations, which can be applied to other businesses looking to improve their customer experience. By leveraging the power of JaamSim, Python, and Excel for data analysis, businesses can make better decisions and create better experiences for their customers. By implementing our recommendations, Z Beans Coffee Shop can continue providing high-quality service and attracting diverse customers while promoting ethical and sustainable practices.

## 2. Problem Description 

Z Beans Coffee Shop has experienced challenges managing customer flow and providing efficient service, particularly during peak hours. The shop's limited staffing, with only one server, cashier, and prep person, has resulted in long wait times and customer frustration, negatively impacting the business's reputation and customer loyalty. Additionally, customer dwell time results in missed revenue opportunities and decreased customer satisfaction.

## 3.Model implementation

### 3.1 Process flow 

![image](https://user-images.githubusercontent.com/80241823/221756651-483de598-d66b-498e-8219-aad4e454ae83.png)
 
Customers entering Z Beans coffee shop follow an exponential distribution with a mean of 4 minutes. The time customers spend placing their orders follows a normal distribution with an average of 3-8 minutes. The time customers spend waiting for their orders to be ready follows a uniform distribution with an average of 1-7 minutes. Dine-in customers enter a separate queue and exit through the exit door after finishing their meal. Customers may choose to join any queue based on their preference. 35% of customers opt for takeaways, and 65% opt for dine-in, with the decision following a discrete distribution. If the queue length exceeds 6, customers exit without placing an order.

### 3.2. Data collection and statistical analysis 

In our analysis of customer behavior at Z Beans Coffee Shop, we did not utilize any qualitative data collection methods such as surveys or interviews. Instead, we relied solely on quantitative data collection methods such as observation to collect data on customer behavior.
Through observation, we collected data on several aspects of customer behavior, such as order size, waiting time, and duration of stay. In addition, during our site visits, we documented many issues related to customer flow, such as bottlenecks or congestion. 
The quantitative data we collected through observation, such as the number of customers served per hour, the interarrival time, the time spent in line, time spent at the counter, prep time for orders, and dwell time, was sufficient to develop the simulation model in JaamSim. A sample size of 100 is sufficient for the research question's complexity. 

### 3.3. Assumptions 

We made several assumptions based on the outputs of statistical analysis about the distribution of data:
•	Customer arrival follows an exponential distribution.
•	Service time for orders follows a normal distribution.
•	Order pick-up follows a uniform distribution. 
•	Customer dwell time follows a normal distribution. 

We also made some assumptions in the process flow to simplify the problem. 
•	Customers are served on a first-come, first-served basis and join the line immediately upon arrival. 
•	The coffee shop has limited tables, and customers who cannot find seating will use takeaway. 
•	Upon arrival, if the queue line is greater than six, then customers exit.

### 3.4. JaamSim Simulation Model Implementation: 

![image](https://user-images.githubusercontent.com/80241823/221756713-998b3080-ca93-4215-a8c1-5d2188ff03e0.png)
 
To implement the JaamSim simulation model for Z Beans Coffee, we used several objects to replicate the coffee shop environment. These objects included: Source, Queue, Server, ResourcePool, Table, and Exit.

### 3.5. Simulation Run 

We declared ten replications for 9 hours (540 minutes) in our Z Beans Coffee Shop simulation model. In addition, we collected data on several performance measures of interest to evaluate the current system's performance, as specified in the problem statement. These measures include the average time customers spent in line, the average time customers spent at the dining table, and the average number of customers served per hour. We also calculated each measure's minimum and maximum values and the 95% confidence intervals. Finally, the time unit used was minutes. 

### 4. Simulations Results 

Table: Performance measures for the current system
Measure	Average	Minimum	Maximum	95% Confidence Interval
Time in line (minutes)	4 	3	30	[3.74, 4.26]
Time at the dining table (minutes)	41.5	20	65	[38.46, 44.54]
Customers served per hour	20	7	32	[17.57, 22.43]
Based on the results from our simulation model, we observe that the average time customers spend in line is 4 minutes, which is relatively short, but the maximum time of 30 minutes is longer than desirable, indicating that some customers may experience long wait times during peak hours. In addition, the average time customers spend at the dining table is 41.5 minutes, which is within a reasonable range, but the maximum time of 65 minutes is longer than optimal, indicating that some customers may stay longer than necessary, reducing table turnover. Finally, the average number of customers served per hour is 20, which is reasonable, but the minimum value of 7 indicates that some hours may be slower than others, which could be a concern for business operations.

### 5. Conclusion

In this project, we analyzed customer behavior at Z Beans Coffee Shop on the Mercer University campus in Atlanta, utilizing JaamSim simulation software to model and analyze customer flow and satisfaction. Through data and sensitivity analysis, we identified potential bottlenecks and areas for improvement in the coffee shop's operations, particularly regarding staffing levels and table access.

The potential implications of our analysis are significant. By implementing our recommendations, Z Beans Coffee Shop can enhance the customer experience and increase customer satisfaction, which could lead to increased loyalty, positive word-of-mouth, and, ultimately, increased profitability. In addition, the coffee shop can improve efficiency, reduce operational costs, and maximize revenue by optimizing customer flow and reducing wait times. Additionally, the coffee shop can better understand customer needs and preferences, leading to a more targeted and effective marketing strategy.

If the manager implements our recommendations, we will propose the following steps to operationalize them. First, we recommend increasing staffing levels to reduce wait times and improve customer flow. This action could involve hiring additional servers, cashiers, and prep persons to accommodate demand. Second, we would suggest streamlining the ordering process by removing items that are less popular or take longer to prepare, which can reduce customer wait time. Finally, we recommend ongoing monitoring and data analysis to ensure that the changes are effective and that the coffee shop continuously improves the customer experience. Z Beans Coffee Shop can implement our recommendations effectively and sustainably by following these steps.

### 6. Recommendations

The recommendations for Z Beans Coffee Shop based on our analysis of customer behavior are as follows:

•	Dedicated parking for takeout orders: Z Beans Coffee Shop could designate a specific area to streamline the takeout ordering process and reduce congestion within the shop. This would allow customers to park easily, place their orders, and pick up their orders without entering the shop, which can help to reduce wait times and improve customer flow.

•	Posting Menu Outside Coffee Shop: Z Beans Coffee Shop could post the menu outside the shop to avoid the bottleneck when customers enter and wait before entering the queue. This would allow customers to decide on their order before entering the shop, reducing the time spent in line and improving customer flow.

•	Increasing personnel: Z Beans Coffee Shop could consider increasing staffing levels to improve customer flow and reduce wait times. This could include adding servers, cashiers, or prep personnel to streamline the ordering process and provide better customer service.

•	Discouraging patrons from occupying tables without making a purchase: To increase the table turnover and accommodate more customers, Z Beans Coffee Shop could discourage patrons from occupying tables without purchasing by clearly stating the policy on the table or through staff communication.

•	Publicize the conference room availability for extended study sessions: To increase customer satisfaction and loyalty, Z Beans Coffee Shop could publicize the availability of a conference room for extended study sessions. Z Beans can achieve this through marketing and communication efforts to the university community, which could help to attract more customers and increase business.

By implementing these recommendations, Z Beans Coffee Shop can improve the customer experience and enhance its operations. These changes can help to increase customer satisfaction, reduce wait times, and ultimately increase profitability.

## Discussion

Our study of customer behavior at the Z Beans Coffee shop has provided valuable insights into how the business can optimize its operations and improve customer satisfaction. Our findings suggest that improving staffing levels, adding popular items to the menu, and improving customer service are key factors in achieving these goals.

However, some limitations to our study to consider. First, our study was conducted over a relatively short time and may not fully capture seasonal variations in customer behavior. Second, our sample size was 100 and may not fully represent the broader customer population. Finally, our study was conducted during peak hours and may not fully capture customer behavior during other times of the day or the weekends.

Despite these limitations, our study provides a useful starting point for further research and optimization of the Z Beans Coffee shop business. By addressing the key findings and recommendations from our study, the business can improve its operations and better meet the needs of its customers

## Conclusion

In conclusion, our study of customer behavior at the Z Beans Coffee shop has identified key factors that can help optimize the business and improve customer satisfaction. By increasing staffing levels during peak hours, adding popular items to the menu, and improving customer service, the business can reduce wait times, increase sales, and improve customer loyalty.

To achieve these goals, it is important for the Z Beans shop management to carefully consider the findings and recommendations from our study and take appropriate action to implement them. Further research may also be needed to fully understand the complexities of customer behavior and identify additional optimization opportunities. Our study demonstrates the value of understanding customer behavior in optimizing business operations and provides a useful model for future studies.
 
 
## Appendices
 
![image](https://user-images.githubusercontent.com/80241823/221756821-f4ba8d8b-52ec-4438-a3a6-d14ee8526dad.png)

![image](https://user-images.githubusercontent.com/80241823/221756843-ab3a897c-13ef-4688-8136-3cb82cc088dc.png)

![image](https://user-images.githubusercontent.com/80241823/221756871-d63ac57c-501f-493c-8828-d66d574f69a9.png)

![image](https://user-images.githubusercontent.com/80241823/221756887-55f72e5f-67ab-44a1-b879-6638dfb8e2c5.png)

![image](https://user-images.githubusercontent.com/80241823/221756913-9c4d3294-5d7d-4e5f-a19f-f7be8f7b7a17.png)

![image](https://user-images.githubusercontent.com/80241823/221756924-4449d1f8-f727-4a25-924d-f40c8e21b0e5.png)

![image](https://user-images.githubusercontent.com/80241823/221756944-71e83503-2805-4a52-bc2f-d299620b6e1f.png)


 
 

 


 

 
 

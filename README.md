### **Objective:** 
This project aims to analyze delivery efficiency factors for Zomato, a leading food delivery platform in India, identifying key variables impacting delivery times and service quality.

### **Approach:**
   - **Inception:** Initiated to optimize delivery operations and enhance customer satisfaction, the project commenced with a comprehensive analysis of available delivery data.
   - **Data Collection:** Gathered datasets encompassing delivery logs, vehicle maintenance records, weather conditions, and delivery person profiles. Utilized S3 for data ingestion and storage.
   - **Data Processing:** Cleaned and validated data using Pandas, and performed distance calculations using the Haversine formula.
   - **Exploratory Data Analysis (EDA):** Utilized Matplotlib for data visualization, including box plots for statistical analysis. Further analysis was conducted using Power BI to identify trends, patterns, and correlations.
   - **Predictive Modeling:** Employed machine learning algorithms from scikit-learn, including XGBoost, Linear Regression, and Random Forest, to predict delivery times with a high level of accuracy.

### **Features and Functionality:**
   - **Distance Calculation:** Implemented the Haversine formula for accurate distance calculations between delivery points.
   - **Weather Integration:** Incorporated weather data to assess its impact on delivery operations.
   - **Traffic Density Analysis:** Analyzed traffic congestion levels to optimize delivery routes and schedules.
   - **Vehicle Conditions and Types:** Considered vehicle conditions (e.g., maintenance status) and types (e.g., bikes, cars) to evaluate their influence on delivery efficiency.
   - **Delivery Person Profiling:** Examined delivery person attributes such as age, experience, and rating to understand their correlation with the time taken to deliver orders.

### **Architecture:**
   - **Data Pipeline:** Developed a robust data pipeline leveraging S3 for ingestion and Redshift for warehousing to handle data processing efficiently.  
   ![redshift](https://github.com/Ashvakg/Zomato-Delivery-Efficiency_Analyzing-and-Predicting-Factors/assets/83398283/b0f5ed53-93b4-49cd-8344-92f6c6d57949)
     
   - **Machine Learning Models:** Utilized scikit-learn for building accurate predictive models for estimating delivery times.
     ( Refer: Zomato_Predicted.csv to view the data and Prediction_XGBoost for the algorithm, Linearregression)
      - Linear Regression: with features Delivery_Person_Age, Ratings, Distance(Calculated using Haversine) Mae of 6.5
      - Random Forest: Considering Features and with RFE(Ranking top 5 feautes)  Delivery_Person_Age, Ratings, Distance (Calculated using Haversine), Road_traffic_density, Vehicle_condition, Type_of_vehicle - Mae of 5.2
      - XGBoost with Considering features: Delivery_person_Age, Delivery_person_Ratings, Weather_conditions, Road_traffic_density, Vehicle_condition, Type_of_vehicle, Distance_km, City_Type, Type_of_order - Mae of 4.8
   
   - **Visualization Tools:** Leveraged Matplotlib for visualizations during EDA and Power BI for more comprehensive visualizations and insights.

   Plot_1: Box plot showing distribution of vehicles by vehicle condition and time taken in minutes
   ![image](https://github.com/Ashvakg/Zomato-Insights/assets/83398283/c0a151be-96ec-4be4-bb8b-3afea0a47032)
   
   plot_2: Top 10 Cities with shortest time taken to deliver an order
   ![image](https://github.com/Ashvakg/Zomato-Insights/assets/83398283/a665379a-5265-4372-8820-ac7eaf4748a0)
   
   plot_3: Scatterplot illustrating correlation between time taken to deliver and road traffic density
   ![image](https://github.com/Ashvakg/Zomato-Insights/assets/83398283/e0b77665-55d7-49b9-804e-43cecdc7042c)

### **Outcomes:**
   - **Key Findings:** Identified significant factors impacting delivery efficiency, including weather conditions, traffic density, and delivery person attributes.
   - **Predictive Accuracy:** Achieved a 98% accuracy rate in predicting delivery times using machine learning models.
   - **Insights:** Uncovered actionable insights for optimizing delivery operations and enhancing service quality.

   ![zomato_Insights_page-0001](https://github.com/Ashvakg/Zomato-Delivery-Efficiency_Analyzing-and-Predicting-Factors/assets/83398283/46eea623-c5fb-4219-8c06-1021d681e441) 

In the first half of March in Chennai, 
   - Bicycles consistently outpaced motorcycles delivery time, indicating potential issues with motorcycle condition or efficiency
   - With nearly 37% of deliveries being made by motorcycles, which are in poor condition are resulting in increased average delivery time.
   - Additionally, vehicles in better condition delivered faster, underscoring importance of regular maintenance.
   - We noted a correlation between sunny weather (usually the case in Chennai during March), higher success rates and faster deliveries.
   - Furthermore, a direct link between road traffic density and delivery time was evident, highlighting the importance of real-time traffic data for route planning.
   - The intermittent spikes and drops in delivery success rates suggest potential external factors influencing delivery performance such as traffic patterns or order volume fluctuations, warranting further investigation for optimized scheduling and resource allocation

### **Future Scope:**
   - **Refinement of Predictive Models:** Continuously refine predictive models and analytical techniques to improve accuracy and adapt to evolving business needs.
   - **Real-Time Monitoring:** Explore real-time monitoring capabilities to track delivery operations and adjust strategies dynamically.
   - **Delivery Optimization Strategies:** Investigate route optimization algorithms and scheduling techniques to further enhance delivery efficiency and customer satisfaction.


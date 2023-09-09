# **Project Name**

### **Exploratory Data Analysis - Hotel Booking**

#### Programming language: Python
#### Libraries used: Numpy, Pandas, Matplotlib, Seaborn 
#### NoteBook: Google Colab
#### Dataset Source: Provided by AlmaBetter


## **Project Summary-**

*In the realm of hotel bookings and hospitality management, a comprehensive analysis can yield valuable insights into guest behaviors, preferences, and industry trends. This project aims to unravel the nuances(opinion) of hotel bookings by employing a diverse array of data exploration and analysis techniques. The dataset has features such as booking cancellations, lead times, guest demographics, and reservation details, offers a wealth of information to be unearthed.*


## **Problem Statement-**

*In the dynamic landscape of hotel management, understanding the complexities of booking behaviors, cancellations, guest preferences, uncovering seasonal trends, understanding guest demographics, deciphering the role of booking channels, optimizing operational efficiency and enhancing guest satisfaction. Resulting in optimized operational strategies, predicting booking cancellations, identifying influential factors, and tailoring services to meet guest expectations and a competitive edge in the ever-evolving world of hospitality management.*


## **Business Objective**

*The primary business objective for hotel booking is to optimize revenue generation, operational efficiency, and guest satisfaction by leveraging data-driven insights and strategies. This encompasses several specific goals aimed to achieving sustainable growth and providing exceptional experiences to guests*


## Dataset

Dataset contains information for City Hotel and Resort Hotel:

* **hotel:** Type of hotel (resort hotel or city hotel)

* **is_canceled:** Indicates whether the booking was canceled (1) or not (0).

* **lead_time:** Number of days that elapsed between the entering date of booking into the PMS and the arrival date.
* **arrival_date_year:** Year of arrival.
* **arrival_date_month:** Month of arrival.
* **arrival_date_week_number:** Week number of the year for arrival.
* **arrival_date_day_of_month:** Date of arrival in that month.
* **stays_in_weekend_nights:** Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at hotel.
* **stays_in_week_nights:** Number of weeknights(Monday to Friday) the guest stayed or booked to stay at hotel.
* **adults:** number of adults among the guests.
* **children:** number of children among the guests.
* **babies:** Number of babies among the guests.
* **meal:** Type of meal opted during stay.
* **country:** Country of origin of the guest.
* **market_segment:** designation of market segment.
* **distribution_channel:** Name of Booking distribution channel.
* **is_repeated_guest:** Indicates if the guest is a repeated guest (1) or not repeated guest (0).
* **previous_cancellations:** Number of previous booking cancellations by the guest prior to current booking.
* **previous_bookings_not_canceled:** Number of previous bookings not cancelled by the guest prior to current booking.
* **reserved_room_type:** Code of the room type reserved.
* **assigned_room_type:** Code of the room type assigned.
* **booking_changes:** Number of changes made to the booking.
* **deposit_type:** Type of deposit made for the booking.
* **agent:** ID of the travel agent making the booking.
* **company:** ID of the company/entity making the booking.
* **days_in_waiting_list:** Number of days the booking was in the waiting list before confirmed.
* **customer_type:** Type of booking, such as transient, contract, group, or other.
* **adr:** Average daily rate.
* **required_car_parking_spaces:** Number of car parking spaces required by the client.
* **total_of_special_requests:** Number of special requests made by the guest.
* **reservation_status:** Current status of the reservation.
* **reservation_status_date:** Date at which the last status was updated.


- Total number of rows in data: 119390
- Total number of columns: 32

## **Data Wrangling**

**1. Duplicates rows were investigated within the dataset:** The initial dataset comprised 119,390 rows, and subsequent removal of duplicate entries resulted in 87,396 remaining rows.

**2. Handling cleaning & missing values:**

**2.1** The "Company" column contains a null values of 82,137 out off 87,396 which is 94%. This level of missing data can significantly impact the accuracy and reliability of analysis performed on data set, Hence delete the company column makes sense.

**2.2** The "agent" column represents agent ID, column contains 12,193 null values out of 87,396 which is 14%. this indicates that there was no assigned agent for that particular bookings, by replacing null with 0, the column remains consistent interms of data type(integer) and can be included in data manipulation without issues related to missing data.

**2.3** The "Country" column represents country code of hotel, column contains 452 null values out of 87,396 which is 0.52%, country code for these hotels were missing, by replacing null values with 'others', the column remains consistent interms of data type(string) and can be included in data manipulations without issues related to missing data.

**2.4** The "Children" column represents number of children stayed at hotel along with adults. column contains 4 null values out of 87,396 which is very less, by replacing null values with 0.

therefore by this step we have removed all duplicated rows and null values in each column were replaced.

**3. Type casting:**

type casting involves changing the data type of a variable or value from one type to another, it plays a crucial role in data manipulation like data compatibility, data integrity and mathematical operations

**4. column assignment/adding:**

- A new column has been assigned "total guests" it represents total count of guests, by adding following columns "adults", "children", "babies."
- A new column has been assigned "total stay" it represents total count of stay in days, by assing following columns "stay in weekend nights" & "stay in week nights."

**5. Removing Outlier:**
Outliers are data points that significantly deviate from the majority of data points in dataset, these extreme values can distort statistical measures and models. leading to inaccurate or biased results.
Here after obeserving the plot majority data points in average daily rate is around 500 units and only on data point is above 5000 which doesn't make any sense, hence removing the outlier. *by this step total rows are 87,395 and columns are 33*

## Data Vizualization, Storytelling & Experimenting with charts : Understand the relationships between variables
#### **Univariate Analysis -**

Chart - 1 City Hotel vs. Resort hotel bookings Analysis

Chart - 2 Seasonal and Yearly Hotel Booking Patterns

Chart - 3 Average Daily Rate Analysis

Chart - 4 Booking Channel preferrence Analysis

Chart - 5 Meal Preference Analysis

Chart - 6 Customer Type Analysis

Chart - 7 Repeated Guests Analysis

Chart - 8 Booking Confirmation Time

Chart - 9 Booking Analysis by weekday or weekend

#### **Bivariate Analysis -**
Chart - 10 ADR Across Distribution Channel

Chart - 11 Room Type Preferences Analysis

Chart - 12 Special Requests Analysis

Chart - 13 Booking Cancellation Across Hotels Analysis

Chart - 14 Booking Changes Analysis

Chart - 15 Booking Cancelation Analysis by Deposit type

#### **Multi-variate Analysis -**
Chart - 16 Correlation Heatmap

Chart - 17 Pair Plots for various columns

## **Solution To Business Objective**
*Marketing and Promotion:* Develop targeted marketing campaigns to attract a diverse range of customers, such as families, couples, and corporate groups. Leverage online and offline marketing channels, including social media, email marketing, and partnerships with travel agencies.

**Analysing guests preferences:** Utilize data analytics to gain insights into guest preferences and behavior. Analyze booking patterns, customer reviews, and historical data to make informed decisions about pricing policies, promotions, and service improvements.

**Pricing Strategy:** Implement dynamic pricing strategies to optimize room rates based on demand and seasonality. Offer packages and discounts during off-peak periods to attract more visitors. Stay informed about industry trends and the competitive landscape. Adapt to changing consumer preferences.

**Diversification of Revenue Streams:** Explore opportunities to generate additional revenue, such as hosting events, offering spa services, or partnering with local businesses for tours and activities.

**Reduce Operational Costs:** Implement energy-saving practices and eco-friendly initiatives, Streamline housekeeping schedules for efficiency, Evaluating and optimize the supply chain for food and beverage services. Invest in energy-efficient technologies like lighting and HVAC systems. Use automated check-in and check-out procedures to reduce manpower.

**Online Reputation Management:** Monitor and respond to guest reviews and feedback on platforms like TripAdvisor and Yelp. Address concerns promptly and use positive feedback as testimonials in marketing materials.

**Staff Training:** Invest in staff training and development to ensure high-quality service. Happy and well-trained employees contribute to positive guest experiences.

**Customer Experience Enhancement:** Continuously improve the guest experience to encourage return visits and positive reviews. This can include personalized services, exceptional dining experiences, recreational activities, and maintaining high cleanliness standards.

**Customer Relationship Management (CRM):** Implement a CRM system to manage guest information and preferences. Use this data to provide personalized experiences, including room preferences, special occasions, and loyalty programs.

## **Conclusion**

**1. City Hotel vs. Resort Hotel Bookings:** City hotels have a higher proportion of bookings (61%) compared to resort hotels (39%), indicating that city hotels are more popular among guests. This insight can guide marketing strategies and resource allocation.

**2. Seasonal and Yearly Hotel Booking Patterns:** Bookings were highest in the year 2016, but the reasons for this peak are unclear.
There are seasonal patterns with higher bookings in July and August and lower bookings in November, December, and January. These insights can help with staff scheduling and inventory management.

**3. Average Daily Rate (ADR) Comparison:** City hotels have a higher overall mean ADR (110.89) compared to resort hotels (99.03), suggesting that city hotels can potentially command higher room rates. Pricing strategies can be adjusted accordingly.

**4. Booking Channel Preference:** The majority of bookings (79.11%) come through Travel Agents/Tour Operators (TA/TO), highlighting their significance. Encouraging more direct bookings (14.86%) can be cost-effective. Maintaining strong relationships with TA/TO partners is crucial.

**5. Room Type Preferences:** Guests tend to prefer room types 'A' and 'D' followed by 'E,' 'F,' and 'G' in both reserved and assigned room types. This information can inform room allocation strategies and renovations.

**6. Meal Preference:** "Bed and Breakfast" (BB) is the most popular meal plan (79.62%), followed by "Self-Catering" (SC) and "Half Board" (HB). Focusing on promoting these preferred meal plans can increase revenue.

**7. Customer Type Analysis:** "Transient" customers constitute the majority (82.36%), followed by "Transient-Party," "Contract," and "Group." Tailoring services to the preferences of the predominant customer type can enhance guest satisfaction.

**8. Repeated Guests:** The analysis reveals a significant dominance of "New booking" (96.09%) over "Repeated booking" (3.91%). Implementing loyalty programs and incentives for repeated bookings can be explored to increase guest retention.

**9. Special Requests During Booking:** A significant portion of bookings (54.6%) do not have any special requests, while 36.1% have only one special request, and a smaller percentage have multiple special requests. Hotel management can optimize resources and services based on the prevalence of special requests.

**10. Booking Cancellation Analysis:**
- High cancellation rates (63,371) compared to non-canceled bookings (24,024) suggest a relatively high booking cancellation rate.
- Potential revenue loss due to canceled bookings emphasizes the need to manage and reduce cancellations through strategies like flexible cancellation policies.

**11. Booking Changes Analysis:** The data shows that a substantial number of bookings (71,494) have no changes, indicating stability in initial reservations. Monitoring patterns of booking changes can help improve booking management processes.

**12. Booking Confirmation Time:** Guests at the "City Hotel" typically experience a longer waiting time (approximately 1.02 days) in the waiting list compared to guests at the "Resort Hotel" (approximately 0.32 days). This insight highlights the importance of efficient reservation handling and waitlist management, particularly for city hotels.

**13. Booking Cancelation Analysis by Deposit type:** Deposit types for guests at both City and Resort hotels are detailed:

- "No Deposit" is the most common deposit type in both hotel types, highlighting the importance of flexible booking options.
- "Non Refund" is also prevalent, indicating a subset of non-refundable bookings.
- "Refundable" deposits are less common but still present, giving guests flexibility in their booking choices. This information can inform deposit policies and marketing strategies.


These conclusions provide valuable insights for decision-making in areas such as marketing, pricing, service offerings, and customer relationship management within the hotel business.

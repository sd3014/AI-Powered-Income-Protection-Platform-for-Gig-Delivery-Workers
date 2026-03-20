# AI-Powered-Income-Protection-Platform-for-Gig-Delivery-Workers
##Introduction

Gig delivery workers are the foundation of modern on-demand logistics. The income of these workers is dependent on their deliveries. Hence, these workers are highly exposed and vulnerable to disruptions such as rainfall, floods, pollution, curfews, and closures of restaurants. The disruptions affect their deliveries and hence their income. Presently, there is no system that compensates workers for these disruptions.

##Problem Statement

Delivery partners, also known as gig workers, are an integral part of the required services, especially in the food delivery and package delivery services. The gig workers are not paid a fixed wage, and their earnings are solely based on the number of deliveries made on a given day. Their earnings are highly variable and depend on the prevailing factors in the environment. Uncertain weather such as heavy rainfall, floods, excessive heat, pollution, traffic restrictions, curfews, or the closure of restaurants can hinder or completely stop the delivery services in a particular region. This forces the gig workers not to make any deliveries, thus they suffer from income loss.
This is more so because gig workers do not enjoy traditional employment benefits such as wages and insurance. Despite the seriousness of this problem, at this moment there is no system in place that is able to identify these disruptions and provide compensation for the lost wages in real time. As such , there is a need for an efficient and intelligent system that is able to identify situations where workers are unable to earn because of external factors and provide them with compensation for their lost wages.

##Proposed Solution

Our system is an AI-based income protection system that works with existing delivery system infrastructure and automatically enables insurance coverage in response to significant reductions in earning opportunities for a delivery worker due to external factors. Instead of depending only on one factor such as weather, our system uses multi-signal detection to recognize actual disturbance in earning opportunities for workers. It analyzes various data sources-weather, traffic, public alerts, and availability of restaurants, to determine whether or not there has been an effect on earning opportunities for workers. The system will only determine that there has been a disruption if all signals indicate abnormal conditions ensuring high accuracy and and reducing false triggers.
Once the worker’s claim of disruption is confirmed, the system immediately calculates the loss in income. The system will then compensate the worker instantly using a parametric insurance system. The entire process is completely automatic, thus there is no need for the worker to make claims. This makes the system efficient, reliable, and user-friendly.

##System workflow

The system follows a structured and automatic workflow to detect disturbance and provide compensation:
1.	Worker registers on the platform
2.	System continuously monitors real-time signals such as:
•	Delivery activity
•	Weather conditions
•	Traffic 
•	Curfews
3.	Delivery activity decrease, disruption alert
4.	Multiple signal confirms disturbance
5.	Calculates expected earnings during non-delivery period based on past data
6.	Records actual earnings during that period
7.	Income loss is calculated
8.	Fraud detection monitors are stimulated
9.	Automatically day’s earning is credited in worker’s account

![WhatsApp Image 2026-03-19 at 23 10 33 (1)](https://github.com/user-attachments/assets/19f2e1cb-c404-4f3b-9d61-11be712e74c7)

##System Architecture

The system architecture is layered, and each component has a specific task to perform to effectively carry out the task of disruption detection and compensation.
Data source layer
This component provides the necessary inputs to the system. It comprises weather data, traffic data, public alerts, trends of delivery activity, and worker GPS data. These data form the basis for disruption detection.
Data collection layer
This component collects data from various sources and processes it for effective use. It fetches the data and processes it for further use.
Disruption detection engine
This is the core component of the system. It processes various data sources such as a drop in delivery activity, weather data, and traffic data to effectively carry out disruption detection. A disruption occurs if the various data sources point to a problem. 
Income calculation engine
This component calculates the worker's expected income and compares it with the actual income earned during the period of disruption. This difference is the income loss.
Fraud detection engine
This module ensures the reliability of the system. It does this by checking the location of the worker, the status of the activity, as well as the history of the claim.
Payout engine
After the disruption has been confirmed, as well as the income loss, the system automatically makes the payment based on the parametric conditions.
Dashboard
Interface for both the workers and admin. Workers can view their earnings, claims, and alerts while admins can view disruptions, claims verifies.

![WhatsApp Image 2026-03-19 at 23 10 33](https://github.com/user-attachments/assets/8e770142-c40e-44dd-81e6-5b87ce96ac77)

##Key modules

1. Disruption detection engine
This module will be used to determine if there is a disruption or not. This will be based on signals. The signals will include the activity of deliveries and external signals, which will include weather conditions, traffic, public alerts, and the availability of restaurants. A disruption will be suspected if there is a reduction in the activities of deliveries. The detection will only be confirmed if there is another supporting signal.
2. Income loss calculation module
This module is designed to calculate the income loss suffered by the worker based on the past and real-time data. The expected earnings are determined based on the average performance of the worker in the past and are then compared with the actual earnings received by the worker during the disruption period. The income loss is then determined as the difference between the expected and actual earnings received.
3. Fraud Detection module
This module ensures the integrity of the system by preventing misuse. It checks for the worker’s location using their GPS to ensure they are in the affected area. It also checks for activity status during the disruption period. In addition, anomaly detection techniques are applied to check for suspicious patterns in claims.
4. Insurance Trigger system	
This module handles the automatic compensation process , using parametric logic. After the confirmation of the disruption and the calculation of income loss, the payment is made based on the application of certain rules and conditions.
5. Parametric Trigger
The system uses some predefined parametric conditions to automatically Detect disturbances and trigger compensation. These triggers are based on real-time data.

Condition	Trigger Type
Delivery activity drop > 60%	 Disruption detected
Rainfall above threshold level	Weather risk
AQI greater than 400	Pollution disruption
Traffic speed below threshold	Movement blockage

##AI/Ml Integration
The system, as proposed, will utilize a variety of AI/ML techniques to achieve the goals of automated disruption detection, income loss estimation, and finally, fraud validation for parametric insurance. The system will utilize multiple sources of data, including weather conditions, traffic congestion, delivery activities, and worker-specific features, including GPS location and historical earnings. A time-series anomaly detection technique, combined with a multi-signal fusion approach, will be used to identify significant disruptions in delivery activities. Techniques, including Isolation Forest or Gradient Boosting, will be used to calculate a disruption score.

The system will then utilize a regression-based approach to calculate approximate earnings based on historical data and subsequently determine income loss by comparing expected and actual earnings. The system will finally utilize a fraud detection component, including rule-based validation and anomaly detection, to validate the authenticity of claims based on location, activities, and historical patterns. The system will operate in a window-based approach, allowing for automated claim triggering and payment without human intervention.

##Tech stack

1.Frontend (User Interface)
Used for worker and admin dashboards.
React.js – for building interactive UI
HTML5, CSS3, JavaScript – basic structure and styling
Tailwind CSS / Bootstrap – responsive design
Chart.js / Recharts – for visualizing earnings, claims, and trends

2.Backend (Server & APIs)
Handles logic, APIs, and communication.
Python (Flask / FastAPI) – backend framework
REST APIs – communication between frontend and backend
JWT Authentication – secure user authentication
Scheduler (Cron Jobs) – periodic data fetching

3. AI/ML Layer
Implements core intelligence of the system.
Scikit-learn – ML models (regression, anomaly detection)
XGBoost / Random Forest – prediction models
Pandas, NumPy – data processing and analysis

4.Data Sources (APIs & Inputs)
Used for real-time signal collection.
OpenWeather API – weather data
AQI API – pollution levels
Google Maps / Traffic API (or mock) – traffic conditions
News API / Public Alerts – curfew, disruptions
Mock Delivery Data – orders per hour simulation

5.Database Layer
Stores user and system data.
MongoDB / PostgreSQL – main database
Collections/Tables:
Users
Earnings History
Disruption Logs
Claims Data

6.Fraud Detection & Validation
Rule-based validation (location, activity)
Isolation Forest / LOF – anomaly detection
Geolocation APIs – GPS verification

7. Payment & Simulation Layer
Razorpay (Test Mode) / Stripe Sandbox – payout simulation
UPI Simulation APIs – optional

8. Deployment & Tools
GitHub – version control
Docker (optional) – containerization
Render / Railway / AWS (optional) – deployment
Postman – API testing

##Future Scope

Further enhancements may include the ability to integrate the delivery platforms and gain access to real-time order and activity data in order to improve the detection of disruptions. The application may be enhanced further through the use of advanced AI techniques like deep learning and time series forecasting in the prediction of disruptions before they occur. The application may be scaled up to work in multiple cities and may be expanded further to include other gig economies like ride-sharing and freelancing. The application may be enhanced further through the introduction of personalized insurance plans based on the behavior of the individual workers. Further, the application may be enhanced through the introduction of adaptive learning and behavioral analytics in the detection of fraud cases. The application may be further enhanced through the introduction of digital payment systems and government alerts.

![WhatsApp Image 2026-03-18 at 23 29 45](https://github.com/user-attachments/assets/2e2981ec-0e94-43cf-a73d-165e1f19766f)
![WhatsApp Image 2026-03-18 at 23 29 43 (2)](https://github.com/user-attachments/assets/6dc0c477-a930-47e0-a4e0-6ae6bc8f4a5c)
![WhatsApp Image 2026-03-18 at 23 29 43 (3)](https://github.com/user-attachments/assets/34784ce3-4023-442d-a682-2024d9b7e8d6)
![WhatsApp Image 2026-03-18 at 23 29 44](https://github.com/user-attachments/assets/cb029948-1f69-4ab6-80ca-65e977c9fde2)
![WhatsApp Image 2026-03-18 at 23 29 44 (1)](https://github.com/user-attachments/assets/795ebaa4-c3e7-4322-b58e-0d74fc8c289f)

#Adversarial Defense & Anti-Spoofing Strategy

##Threat Model

While coming across this problem statement we identified three types of attackers who might target the system. The first is single/individual worker using GPS spoofing tools to fake location data. The second is a coordinated group collaborate via platform like Telegram to exploit the system at scale. They come together to claim synchronized fraudulent claims. The third is the data level attacker who attempts to manipulate data into external APIs to trigger payment. Each of these category require different approach to detect fraud. These includes device-level validation, behavioral pattern analysis, group anomaly detection, and multisource verification. This ensures reliable and robust system security.

##Multi-Layer Defense Architecture

1️⃣ Device & Location Integrity
This layer checks spoofing by analyzing irregularities in location and movement. The system tracks sudden location jumps, unrealistic speed patterns and transition between distant coordinates. It cross checks GPS data with device sensor such as accelerometer and motion signals to look after physical movement and reported location validity. Additionally, it will check GPS coordinates with cell tower and network based positioning to detect the mismatch. Any inconsistency in these factors will be reflected in the risk score. This prevents the fraudulent claims to enter the payout pipeline.

2️⃣ Claim-Level Intelligence
The system analyses each claim separately by using validation based real-world scenarios and behavioural consistencies. The system verifies each claim matches the actual environmental conditions rather than blindly accepting the claims.
The system starts by checking whether the disruption was actually initiated by external factors such as weather conditions, traffic and curfew announcements.
For example , if a worker claims to have suffered loss on a particular day dues to heavy rainfall, the system should be able to confirm if it indeed experienced heavy rain at that time. 
Secondly , it checks for the authenticity of the income loss by comparing it with the earning patterns of the particular employee. If an employee’s average earning per day is ₹300 to ₹500
and suddenly reports a high loss , the system checks for it.	
Finally, a circuit breaker is introduced in the system in the system to prevent mass fraud.
Suddenly if there are a large number of claims triggered from a particular region, the system temporarily suspends all transactions and enters a verification code.

3️⃣ Network & Ring Detection
It has a network-level intelligence component which detects coordinated fraud attacks thus recognizing group malicious activity.
The system will continuously monitor patterns of claims in various regions. If there is a sudden surge in claims from a certain region, especially within a short time frame, it is considered suspicious which might get flagged for further analysis.
Another important indicator that can be verified by the system is related to synchronized claim timing. In many cases of fraud rings, it has been identified that fraudsters tend to submit claims at almost the same time through various coordinated integrated platforms. This can be identified by the system based on the timestamps of the claims received by it. It can identify groups of claims that are made in very close proximity to each other. 
Additionally, the system can also carry out account clustering analysis to identify fraud rings. This can be done based on identifying common behavioral traits in various accounts. In many cases, it has been identified that fraudsters tend to exhibit similar behavior in many accounts. If many accounts exhibit almost similar suspicious behavior, they can be identified as a fraud ring.

4️⃣ Upstream Data Integrity
When you did not collect the data yourself, how can you trust that data? When a delivery driver submits a disruption claim, our system does not rely solely on one weather feed to verify the claim because any single feed could go offline, or lose synchronisation, or worst of all, could be tampered with. In these instances, the system checks weather, traffic, and delivery activity independently at the same time and requires them to all tell the same story before we will accept that there was a disruption. As soon as the sources begin to provide inconsistent information – for example, one source is reporting a storm in one area, while another source is reporting clear skies in that same geographical region – the system will flag the discrepancy, suspend any automated payout, and the case will go to a human to determine if there is indeed a disruption. The logic here is simple: the more independent sources report the same thing, the more certain we are in our actions, and the more difficult it will be for someone to "game" the system by manipulating only a single data point.

##Worker Trust Score

Each worker that has joined the platform is assigned a Trust Score of 0–100 based on their individual circumstances. An employee with a two-year history of consistent deliveries, for example, would be afforded more trust than one who just began delivery work; therefore, their Trust Score would be substantially different. All workers, regardless of how long they have worked on the Platform, will continue to receive Trust Scores; however, their scores may change based on their activity on the platform.

As a result, the background-based Trust Score gives all workers—regardless of their time with the platform or how reliable they've been—an advantage. A worker who is known for delivering consistently would experience almost no verification through the payout process because their payout is initiated immediately after the claim is approved by the system. A worker whose performance history is not well-known would receive a partial payout while a verification continues to take place in real-time. If a worker has a low Worker Trust Score, their claim will be subject to an additional review before a payout is processed, but this is not considered a punishment; it is simply a prudent review period. The goal is to create an easy experience for honest workers and a difficult experience for dishonest workers.

##False Positive Protection

We have to make sure that delivery partners are not denied during real disturbance. In many situations, such as rain, bad network or issues with the GPS may affect the accuracy of tracking. Also we have to reduce the detection thresholds at the time of real events of significant disruption. The main doubt benefits would be only given to the workers whom we can trust and have a proper experience. We have to make our system transparent with a mechanism for our delivery partners to appeal. Our main priority should be to prioritize the authentic delivery partners and block all the other possible cases of fraud.

## Adaptive Learning

We learn from the claims done in the past and cases of fraud to constantly improve the system. We train again and again the AI model by using the original fraud data. So, based on the new patterns the adjustment of the threshold will be done for detection. Modifying the changes in the behavior of the user and new techniques for fraud. The system we make should be smarter, more dependable, and which becomes difficult to exploit over the period of time. Guarantee the long-term legitimate and organized way for the claim of detection and decisions of payouts.









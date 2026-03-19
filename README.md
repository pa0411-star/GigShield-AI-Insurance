 Problem Statement:

India’s gig economy relies heavily on delivery partners working for platforms like Swiggy, Zomato, and other on-demand services. These workers earn on a daily basis, making their income highly dependent on consistent working hours.
However, their ability to work is often disrupted by external conditions beyond their control, such as:
*  Heavy rain and floods  
*  Extreme heat conditions  
*  High air pollution levels  
*  Curfews, strikes, and government restrictions  

During such events, delivery activity slows down or stops completely. Even though workers are willing to work, they are unable to do so, resulting in direct income loss.
Currently, there is no dedicated insurance or financial safety system that protects gig workers from these types of disruptions. Traditional insurance products focus on health, accidents, or vehicle damage, but do not address the loss of daily earnings caused by external environmental and social factors.
This creates a major gap where gig workers are left financially vulnerable whenever such disruptions occur.
Our project aims to solve this problem by designing an AI-powered parametric insurance platform that automatically detects these disruptions and provides instant income protection, without requiring manual claims.

Target Persona:

Our solution is designed for food delivery partners working on platforms like Swiggy and Zomato in urban areas.

 Persona Profile
* Role: Delivery Partner (Gig Worker)  
* Age Group: 20–40 years  
* Work Type: Full-time / Part-time delivery  
* Location: Urban and semi-urban cities (e.g., Chennai)  

Work Pattern
* Works 8–10 hours per day  
* Completes 15–25 deliveries daily  
* Peak working hours:
  - Lunch (12 PM – 2 PM)  
  - Dinner (7 PM – 10 PM)  
* Depends on daily order availability  

 Income Details
* Average daily earnings: ₹600 – ₹1000  
* Weekly earnings: ₹4000 – ₹7000  
* Income varies based on:
  - Demand  
  - Weather conditions  
  - Working hours  

 Key Problems Faced
  Delivery partners frequently lose income due to
    *  Heavy rain and flooding  
    *  Extreme heat making outdoor work difficult  
    *  High pollution levels  
    *  Curfews, strikes, or restricted zones  
    *  Sudden drop in orders due to external conditions  
Even when they are ready to work, they are unable to earn due to these disruptions.

 

 Parametric Triggers:

Our system does not rely on a single data point (like GPS or weather) to trigger payouts.  
Instead, we use multi-layer parametric triggers, combining environmental, behavioral, and platform signals.

Environmental Triggers
* Rainfall > threshold (e.g., 50mm/hour)
* Temperature > 42°C (extreme heat)
* AQI > 300 (severe pollution)
* Flood alerts / waterlogging data

Social & Operational Triggers
* Curfew or government restriction alerts
* Local strikes or zone closures
* Restaurant/store activity drop > 40%

Activity-Based Triggers (Critical Layer)
* Drop in orders/hour compared to historical average
* Reduction in active delivery partners in the same zone
*Platform-level slowdown (simulated API data)

Multi-Condition Trigger Logic
  Payouts are triggered only when multiple conditions are satisfied together, for example
    * Severe rain detected  
    * AND delivery activity drops significantly  
    * AND multiple workers in the same zone are affected  
This prevents false claims based on a single manipulated signal.

 
  
 Weekly Pricing Model:

Our platform follows a dynamic weekly pricing model, designed specifically for gig workers whose earnings are short-term, variable, and highly sensitive to external disruptions.
Unlike traditional insurance, which relies on fixed premiums and long-term policies, our model is

*  Weekly-based (aligned with gig income cycles)  
*  AI-driven (risk-adjusted pricing)  
*  Adaptive (updates based on real-world conditions)  

Core Pricing Principle
  The weekly premium is calculated using a risk-based scoring system, where each worker is assigned a dynamic risk score.

Risk Score Factors:
* Location Risk : flood-prone, high-traffic, pollution-heavy zones
*   Environmental Risk : rainfall, heat index, AQI trends  
* Disruption Frequency : past incidents in that area  
*  Work Pattern : working hours, delivery consistency  
*  Time-Based Risk : peak vs off-peak dependency  

 
 Payout Calculation
      Payouts are based on actual income loss
       Payout = average hourly income × hours affected

This ensures
* Accurate compensation  
* No fixed or arbitrary payouts  
* Direct linkage to worker earnings  

 Dynamic Weekly Adjustment
    Premiums are recalculated every week based on:
      * Weather forecast changes  
      * Increase/decrease in disruption frequency  
      * Area-level risk updates  
      * Worker activity consistency  
This allows the system to stay responsive and fair.

Financial Sustainability (Important Layer)
  To prevent system abuse and ensure long-term viability
    * Risk-based pricing balances high-risk users  
    * Coverage limits are enforced per plan  
    * Multi-condition triggers prevent false payouts  
    * Fraud detection reduces invalid claims  

Adversarial Defense & Anti-Spoofing Strategy
    Recent threat scenarios highlight the risk of coordinated fraud using GPS spoofing.  
    Our system is designed with a multi-layer AI-powered defense architecture to detect, prevent, and respond to such attacks in real time.

  AI Integration Overview
    At the core of our system is an AI-driven fraud detection engine that continuously analyzes user behavior, environmental data, and network-level patterns.

  The AI system performs:
    * Real-time anomaly detection  
    * Behavioral pattern analysis  
    * Multi-signal validation  
    * Risk scoring for each claim  
Each claim is assigned a Fraud Risk Score, which determines how it is processed.

Differentiation: Genuine Worker vs Spoofed User
  Instead of trusting location alone, our AI model analyzes **behavioral consistency over time**.


AI Approach:

* Time-Series Analysis → Tracks movement history and activity patterns  
* Anomaly Detection Models → Identifies unusual location or behavior spikes  
* Clustering Algorithms → Compares user behavior with nearby workers  

Genuine Worker Pattern

* Continuous movement before disruption  
* Active delivery sessions  
* Gradual drop in activity  
* Similar impact across nearby workers  

 Spoofed User Pattern

* Sudden unrealistic location jumps  
* No delivery activity before claim  
*  Static or inconsistent movement  
*Mismatch with surrounding worker activity  

 The AI classifies each claim into:
* Valid  
* Suspicious  
* High-risk  

Data Signals Used (Beyond GPS)
  Our AI engine combines multiple data streams to make accurate decisions

Device & Location Intelligence
*  GPS consistency over time  
*  Speed, direction, and movement continuity  
*  Device fingerprinting (device ID patterns)  

Platform Activity Data
* Number of deliveries completed  
* Active session logs  
* Order acceptance and completion rates  

Environmental Cross-Verification
* Weather API vs actual claim location  
* Severity of disruption in that zone  
* Area-wide delivery drop  

Network-Level Detection (AI-Driven)
* Cluster Detection Models identify
  - Multiple users showing identical patterns  
  - Sudden surge of claims from same region  
* Graph-based analysis detects coordinated fraud rings  

UX Balance: Handling Flagged Claims Fairly
We ensure security without affecting genuine users.

Normal Claims
* Automatically approved  
* Instant payout  

Suspicious Claims
* Temporarily held  
* AI triggers secondary verification  
* User notified:
  - "We are verifying your claim due to unusual activity"

High-Risk Claims
* Blocked automatically  
* Sent for admin review  


Tech Stack:

Our platform is built using a modern, scalable architecture that combines frontend, backend, AI/ML, and real-time data integrations to deliver a seamless 
and intelligent insurance system.

Frontend (User Interface)
* React.js  
* HTML, CSS, JavaScript  

The frontend provides a simple and user-friendly interface where delivery partners can:
* Register and onboard easily  
* Select weekly insurance plans  
* Track active coverage  
* View claim status and payouts  

Backend (Application Layer)
* Node.js
*  Express.js  

The backend handles core system logic, including
* User authentication and profile management  
* Policy creation and management  
* Claim processing and payout triggering  
* API integrations and data aggregation  

 AI / Machine Learning Layer
* Python  
* Scikit-learn  

AI models are used for:
* Risk assessment and premium calculation
* Income estimation based on work patterns  
* Fraud detection using anomaly detection techniques  
* Anti-spoofing analysis using behavioral data  

Database
* MongoDB  

Used to store:
* User profiles  
* Insurance policies  
* Claims and transaction history  
* Risk and activity data  

APIs & External Data Integration

To enable real-time parametric triggers, the system integrates multiple APIs

*  Weather APIs → rainfall, temperature, flood alerts  
*  Air Quality APIs → pollution levels  
*  Government / public datasets → curfews, restrictions  
*  Simulated platform APIs → restaurant/store activity  
*  Mock APIs → fuel availability and disruptions  

Payment Integration (Simulation)
* Razorpay (Test Mode) / UPI Simulation  
Used for:
* Instant payout demonstration  
* Secure transaction flow  
* Claim-to-payout automation  

Fraud Detection & Security Layer
* AI-based anomaly detection  
* Multi-signal validation system  
* Device and location verification logic  

This layer ensures protection against
* GPS spoofing  
* Fake claims  
* Coordinated fraud attacks  


System Workflow:

Our platform follows a **fully automated, AI-driven workflow** that ensures seamless insurance coverage, real-time disruption detection, and instant payouts.
User Onboarding
 Delivery partner registers on the platform  
* Provides:
  - Name, phone number  
  - Delivery platform (Swiggy / Zomato, etc.)  
  - Location / working zone  
  - Average working hours  
  - Weekly earnings  

AI-Based Risk Profiling
* The system analyzes:
* Location risk (flood-prone, high pollution zones)  
* Historical disruption patterns  
* Worker activity behavior  

Weekly Plan Selection
* User selects a plan (Basic / Standard / Premium)  
* Premium is calculated dynamically based on risk  

Real-Time Monitoring (Core Engine)
The system continuously monitors multiple data sources:
*  Weather APIs → rain, heat, floods  
*  Air quality data → pollution levels  
*  Government alerts → curfews, restrictions  
*  Platform activity → order demand, restaurant activity  

 Multi-Signal Trigger Detection
A disruption is confirmed only when:
- Environmental condition exceeds threshold  
- AND delivery activity drops  
- AND multiple workers are affected  

AI Fraud Detection Layer

Before triggering payout, the system validates the claim:
* Checks movement history and behavior  
* Detects GPS spoofing patterns  
* Compares with nearby worker activity  
* Assigns a Fraud Risk Score

Claim Decision Engine
Based on fraud score:

*  Valid → Auto-approved  
*  Suspicious → Verification required  
*  High-risk → Blocked  

Payout Calculation
The system calculates income loss:
Payout = average hourly income × hours affected  

Instant Payout Processing
* Approved claims are processed instantly
* Payment sent via:
  - UPI / wallet (simulated)  


Conclusion:

Our platform presents a practical and scalable approach to solving one of the most overlooked problems in the gig economy — income loss due to external disruptions.
By combining AI-driven risk assessment, parametric trigger-based automation, and instant payout mechanisms, we eliminate the delays and complexities of traditional insurance systems.

The solution is designed to be:

* Simple for gig workers to use  
* Affordable through a weekly pricing model  
* Reliable with built-in fraud detection and anti-spoofing mechanisms  
* Scalable across different delivery platforms and regions  

Most importantly, it focuses on what truly matters — protecting the daily earnings of gig workers when they are unable to work due to conditions beyond their control.
With further development and real-world integration, this system has the potential to become a **financial safety net for millions of gig workers**, making the gig economy more secure and sustainable.




  



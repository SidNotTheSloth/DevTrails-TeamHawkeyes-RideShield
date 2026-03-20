# RideShield - AI-Powered Mobile App Parametric Insurance for Gig Workers

### Protecting Delivery Riders from Income Loss Due to External Disruptions

---

## Problem Understanding

### Chosen Persona
Food delivery riders (e.g., Swiggy/Zomato workers operating in urban areas)

### Core Problem
Delivery riders lose income due to uncontrollable external disruptions like heavy rain, heatwaves, pollution, or curfews, with no system to compensate for lost working hours.

### Impact
- Provide reliable income protection for gig workers  
- Enable insurers to offer a sustainable, data-driven weekly premium model  

---

## User Persona & Scenario

### Persona Description
An urban food delivery rider whose earnings depend on daily deliveries, working hours, and external conditions like weather and demand.

### Sample Scenario
During heavy rainfall, the rider cannot complete deliveries due to unsafe conditions and reduced demand, resulting in significant income loss with no compensation.

---

## Disruptions Covered

| Disruption | Why It Matters |
|----------|----------------|
| Heavy Rain / Floods | Unsafe riding, reduced orders |
| Heatwaves | Reduced working hours, health risk |
| Pollution (AQI) | Government restrictions, health hazard |
| Cyclones / Storms | City-wide shutdowns |
| Curfews / Lockdowns | Movement restrictions |
| Dense Fog | Unsafe visibility conditions |

---

## Parametric Trigger Design

| Event | Trigger Condition | Data Source |
|------|------------------|------------|
| Rainfall | ≥ 15mm/hr or ≥ 50mm/day | OpenWeather API |
| Heatwave | ≥ 42°C for 4+ hours | OpenWeather API |
| AQI | ≥ 300 | CPCB / IQAir |
| Storm | ≥ 90 km/h wind or alert | IMD |
| Fog | Visibility ≤ 50m | Weather API |
| Curfew | Govt order active | Govt APIs |

---

## Weekly Premium Model

### Pricing Plans

| Plan | Premium | Coverage | Max Payout |
|------|--------|----------|------------|
| Basic | ₹15/week | 3 days | ₹300 |
| Standard | ₹25/week | 5 days | ₹500 |
| Premium | ₹40/week | 7 days | ₹800 |

### Pricing Logic
- AI calculates a location-specific risk score  
- Higher risk areas have slightly higher premiums  
- Based on weather patterns, AQI, and disruption history  
- Designed to remain affordable while ensuring insurer sustainability  

---

## AI Integration

### Risk Prediction
- Predicts disruption probability using weather, AQI, and historical data  
- Generates location-based risk scores  

### Dynamic Pricing
- Adjusts weekly premiums based on predicted risk  
- Updated weekly to reflect changing conditions  

### Fraud Detection
- Detects unusual claim patterns  
- Identifies location mismatches  
- Flags claims from inactive users  

### Predictive Insights
- Identifies high-risk zones  
- Forecasts claim volumes  
- Helps optimize pricing strategies  

---

## System Workflow

1. User registers via Flutter app (OTP login)  
2. Selects plan and pays weekly premium  
3. Backend fetches real-time weather and AQI data  
4. AI calculates disruption risk  
5. Trigger conditions are evaluated automatically  
6. Payout is processed instantly and user is notified  

---

## System Architecture

## System Architecture

<p align="center">
  <img src="RideShield - Architecture.jpeg" width="700"/>
</p>

The architecture illustrates the end-to-end flow of the system, from the worker-facing mobile app to backend processing, AI-based risk evaluation, and integration with external data sources for automated parametric payouts.


---

## Tech Stack

- Frontend: Flutter  
- Backend: FastAPI (Python)  
- Database: Firebase Firestore  
- AI/ML: TensorFlow / PyTorch  
- APIs: OpenWeather, AQI, Maps  
- Authentication: Firebase Authentication  
- Notifications: Firebase Cloud Messaging  
- Payments: Razorpay / Stripe  

---

## Platform Design

### Worker App
- OTP-based login  
- Plan selection  
- Weekly payments  
- Live disruption alerts  
- Automatic payout tracking  
- Policy and payout history  

### Admin Dashboard
- Real-time trigger monitoring  
- Policy overview  
- Fraud detection alerts  
- Risk heatmap  
- Financial analytics  

---

## Dashboard & Analytics

### Worker Dashboard
- Active policy status  
- Risk level indicator  
- Weather and AQI conditions  
- Payout history  
- Renewal reminders  

### Admin Dashboard
- Premium vs payout tracking  
- Live disruption map  
- Trigger statistics  
- Risk heatmaps  
- Fraud alerts  
- User growth metrics  

---

## Development Plan

### Phase 1
- Ideation and system design  
- Define pricing and triggers  
- Finalize architecture  

### Phase 2
- Build frontend and backend  
- Integrate APIs  
- Implement trigger logic  

### Phase 3
- Add fraud detection  
- Implement payouts  
- Build dashboards  
- Optimize system  

---

## Unique Value Proposition

- AI-driven parametric insurance tailored for gig workers  
- Fully automated payouts without manual claims  
- Multi-trigger disruption coverage  
- Weekly pricing aligned with gig worker income cycles  
- Scalable micro-insurance model  

---

## Impact

### For Workers
- Income protection during disruptions  
- Reduced financial stress  
- Fast and simple payouts  

### For Platforms
- Improved worker retention  
- More reliable delivery operations  

### For Insurance Industry
- Access to gig economy market  
- Data-driven pricing models  
- Scalable and sustainable solution  

---


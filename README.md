# Qatrah Hayat+ - Blood Donation Management Platform

## Overview
Qatrah Hayat+ is a blood donation management system designed to facilitate blood banks, donors, and emergency services. It provides a platform for donors to schedule appointments, track rewards, and participate in campaigns. Blood banks can manage inventory and receive real-time alerts, while administrators oversee the system through an intuitive dashboard.

---

## Project Plan & Team Structure

### **Frontend Team (React.js)**  
**Tasks:**  
1. Build donor-facing UI (scheduling, rewards, campaigns).  
2. Create blood bank & emergency interfaces (maps, alerts, inventory).  
3. Develop admin dashboard (analytics, CRUD operations).  

### **Backend Team (Node.js + MongoDB)**  
**Tasks:**  
1. Design APIs for blood banks, inventory, and scheduling.  
2. Implement emergency alerts, campaign predictions, and rewards logic.  
3. Set up admin routes, authentication, and data aggregation.  

---

## Project File Structure  

### **Frontend (React.js)**  
```
src/  
├── components/  
│   ├── BloodBankFinder/  
│   │   ├── MapComponent.jsx  
│   │   └── BloodBankCard.jsx  
│   ├── Inventory/  
│   │   ├── BloodTypeChart.jsx  
│   │   └── InventoryTable.jsx  
│   ├── Scheduling/  
│   │   ├── DonationCalendar.jsx  
│   │   └── RecommendationPanel.jsx  
│   ├── Rewards/  
│   │   ├── PointsDisplay.jsx  
│   │   └── PartnerBenefits.jsx  
│   ├── Emergency/  
│   │   ├── AlertBanner.jsx  
│   │   └── EmergencyToggle.jsx  
│   └── Admin/  
│       ├── AnalyticsDashboard.jsx  
│       └── UserManagement.jsx  
├── pages/  
│   ├── DonorDashboard.jsx  
│   ├── BloodBankPortal.jsx  
│   ├── CampaignOrganizer.jsx  
│   └── AdminDashboard.jsx  
├── services/  
│   ├── api.js          // Axios instance for API calls  
│   └── auth.js         // Authentication helpers  
└── App.js              // Routes & layout  
```

### **Backend (Node.js)**  
```
server/  
├── controllers/  
│   ├── bloodBankController.js  
│   ├── inventoryController.js  
│   ├── schedulingController.js  
│   ├── emergencyController.js  
│   ├── rewardsController.js  
│   ├── campaignController.js  
│   └── adminController.js  
├── models/  
│   ├── BloodBank.js  
│   ├── Donation.js  
│   ├── Donor.js  
│   ├── Inventory.js  
│   ├── Campaign.js  
│   └── Reward.js  
├── routes/  
│   ├── bloodBankRoutes.js  
│   ├── inventoryRoutes.js  
│   ├── schedulingRoutes.js  
│   ├── emergencyRoutes.js  
│   ├── rewardsRoutes.js  
│   ├── campaignRoutes.js  
│   └── adminRoutes.js  
├── utils/  
│   ├── predictionService.js  // ML for inventory forecasts  
│   └── alertService.js       // SMS/email integrations  
└── app.js                    // Server setup  
```

---

## Task Breakdown  

### **Frontend Team**  
1. **Frontend Dev 1:**  
   - **Blood Bank Integration:**  
     - Build map UI with real-time blood bank locations (e.g., Google Maps API).  
     - Display inventory status cards with dynamic data.  
   - **Emergency System:**  
     - Create alert banners and emergency toggle UI.  

2. **Frontend Dev 2:**  
   - **Smart Inventory:**  
     - Charts for blood type availability (Chart.js/ApexCharts).  
   - **Scheduling:**  
     - Calendar UI for donation appointments.  
     - Recommendation panels for optimal times.  

3. **Frontend Dev 3:**  
   - **Rewards & Campaigns:**  
     - Points tracker and partner benefit displays.  
     - Campaign creation forms and progress trackers.  
   - **Admin Dashboard:**  
     - Analytics tables/charts and user management UI.  

---

### **Backend Team**  
1. **Backend Dev 1:**  
   - **Blood Bank Integration:**  
     - `/api/bloodbanks` endpoints for location-based queries.  
   - **Inventory Management:**  
     - Aggregation pipelines for rare blood type reports.  
     - Predictive model integration (e.g., Python script via REST).  

2. **Backend Dev 2:**  
   - **Scheduling & Emergency:**  
     - `/api/schedule` endpoints with donation history tracking.  
     - Emergency alert logic (Twilio/SendGrid integration).  
   - **Campaigns:**  
     - Prediction of donation volume (MongoDB aggregations).  

3. **Backend Dev 3:**  
   - **Rewards & Admin:**  
     - Points system logic and partner API integrations.  
     - Admin routes for user/data management (JWT auth).  

---

## Key Implementation Steps  
1. **Setup:**  
   - Initialize React + Node.js projects.  
   - Connect MongoDB Atlas and define schemas.  

2. **Core Features:**  
   - Backend builds blood bank inventory API (Dev 1).  
   - Frontend integrates maps and real-time data (Dev 1).  
   - Predictive model for inventory (Dev 1).  

3. **Scheduling & Rewards:**  
   - Backend creates donation records (Dev 2).  
   - Frontend builds calendar + recommendation UI (Dev 2).  
   - Rewards system API (Dev 3).  

4. **Emergency & Campaigns:**  
   - Alert service with SMS/email (Dev 2).  
   - Campaign prediction logic (Dev 2).  

5. **Admin Dashboard:**  
   - Backend aggregates data for admin routes (Dev 3).  
   - Frontend builds analytics dashboard (Dev 3).  

6. **Testing:**  
   - Use Postman for API testing.  
   - React Testing Library for UI components.  

7. **Deployment:**  
   - Frontend: Netlify/Vercel.  
   - Backend: Heroku/AWS.  

---

## Tools & Dependencies  
- **Frontend:** React Router, Redux, Axios, Chart.js, Leaflet/Mapbox.  
- **Backend:** Express.js, Mongoose, JWT, Twilio/SendGrid, Socket.io (for real-time).  
- **Database:** MongoDB Atlas (cloud hosting).  


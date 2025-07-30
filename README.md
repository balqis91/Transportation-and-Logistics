# 🚚 Transportation and Logistics Analytical Dashboard

## 📌 Overview  
This project analyzes logistics and transportation data using **Power BI** and a relational data model.  
It provides insights into **bookings, shipment types, delivery performance, and vehicle utilization**, helping logistics companies improve efficiency and customer satisfaction.  

The solution includes:  
- 🗄️ **Relational Data Model** with customers, vehicles, routes, and bookings  
- 🔑 **Data Cleaning & Preparation** to ensure reliable insights  
- 📊 **Interactive Power BI Dashboards** for operational monitoring  
- 📈 **Key KPIs** such as total bookings, on-time deliveries, and top booking routes  
- 🌍 **Geospatial Insights** showing booking distribution across India  

---

## 🧹 Data Cleaning & Preparation  

Before building the dashboard, data was cleaned and transformed using **SQL, Power Query, and DAX**:  

1. **Handling Missing Data**  
   - Filled missing shipment details with placeholders.  
   - Ensured all bookings had valid `BookingID`, `CustomerID`, and `VehicleID`.  

2. **Data Type Standardization**  
   - Converted booking dates into `DATE` format.  
   - Normalized city names and vehicle registrations.  

3. **Duplicate Removal**  
   - Removed duplicate booking records based on `BookingID` and `CustomerID`.  

4. **Data Transformation**  
   - Created a **Date Dimension Table** for time-based analysis (day, week, month, year).  
   - Split `OriginLocation` and `DestinationLocation` into **Latitude/Longitude** for mapping.  

5. **New Columns & Measures**  
   - Added a calculated column for **On-Time Delivery Performance**.  
   - Categorized shipments by type (`Regular`, `Market`).  
   - Built DAX measures for **Total Bookings, Daily/Monthly Trends, and Top Routes**.  

---

## 📊 Dashboards  

### Transportation & Logistics Dashboard  
<img width="1107" height="667" alt="image" src="https://github.com/user-attachments/assets/b54231a0-4da1-4f93-beab-eb5afdd70843" />

### Data Model  
<img width="1065" height="667" alt="image" src="https://github.com/user-attachments/assets/1d24f480-aad7-4688-a1ec-7672e26f5129" />


---

## ✅ Database Schema  

**Primary Data Table**
- `BookingID` (PK)  
- `BookingDate`  
- `BookingTime`  
- `CustomerID` (FK → Dim_Customer)  
- `DestinationID` (FK → Dim_Destination)  
- `VehicleID` (FK → Dim_VehicleDetails)  
- `Day`  
- `DayNo`  
- `Destination Latitude`  
- `Destination Longitude`  

**Dim_Customer**
- `CustomerID` (PK)  
- `CustomerName`  
- `BookingID`  
- `MaterialShipped`  

**Dim_VehicleDetails**
- `VehicleID` (PK)  
- `DriverName`  
- `VehicleRegistration`  

**Dim_OriginInformation**
- `OriginID` (PK)  
- `OriginCity`  
- `OriginLocation`  
- `OriginState`  

**Dim_Destination**
- `DestinationID` (PK)  
- `DestinationCity`  
- `DestinationLocation`  

**Dim_Date**
- `Date`  
- `DayOfWeek`  
- `Month`  
- `Quarter`  
- `WeekNumber`  
- `Year`  

---

## 🔍 Key Insights  
- **Total Bookings:** 3,582  
- **Total Customers:** 3,585  
- **On-Time Delivery Leaders:** Kanchipuram, Ahmedabad, Hosur  
- **Top Booking Route:** Kanchipuram with nearly 3,000+ bookings  
- **Shipment Type Distribution:** Regular bookings dominate (99.24%)  
- **Geographical Distribution:** Dense booking clusters across major Indian cities  
- **Vehicle Utilization:** TS15UC9341 most frequently used  

---

## 📌 Conclusion  
The **Transportation and Logistics Dashboard** demonstrates how **Power BI and relational data models** can provide end-to-end visibility into logistics operations.  
This enables companies to:  
- Optimize routes and shipments  
- Improve on-time delivery performance  
- Manage customer demand across regions  
- Track and balance vehicle utilization  

**Future Improvements**
- Integrate real-time GPS tracking  
- Add cost and revenue analytics  
- Predict demand using machine learning  

---

## ⚙️ Tools Used  
- **SQL / Relational Database Modeling** – Fact & dimension tables  
- **Power BI** – Dashboards and interactive visualizations  
- **DAX & Power Query** – Advanced metrics and data cleaning  
- **Geospatial Analysis** – Booking distribution mapping  

---

👩‍💻 Created by *Balikisu Ajoke Oniyide*
# Transportation-and-Logistics

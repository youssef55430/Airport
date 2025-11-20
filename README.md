# 🧭 Customer Satisfaction Analysis – Tourism Company  
Interactive Power BI Dashboard

## 📌 Overview  
This project analyzes customer satisfaction for a tourism company across multiple service categories, including trip quality, hotel experience, transportation, customer support, and overall value for money.  
The dashboard helps the company identify strengths, weaknesses, and improvement opportunities using real data insights.

---

## 🎯 Project Objectives  
- Understand key factors affecting customer satisfaction.  
- Identify low-rated services and root causes.  
- Compare satisfaction levels across regions, customer segments, and trip types.  
- Provide actionable insights to improve service quality.  
- Support data-driven decision making for tourism operations.

---

## 🗂️ Dashboard Features  
### **1️⃣ Key KPIs**
- Average Satisfaction Score  
- Total Number of Respondents  
- % of Satisfied vs Dissatisfied Customers  
- NPS (Net Promoter Score)  
- Repeat Customer Rate  

### **2️⃣ Customer Segmentation**
- Trip Type (Adventure / Family / Luxury / Budget)  
- Region (Egypt – Cairo, Luxor, Sharm El Sheikh, Hurghada… etc.)  
- Age Groups  
- Nationalities  

### **3️⃣ Detailed Views**
- Service Ratings (Hotels, Transport, Tour Guides, Customer Service)  
- Complaint Analysis  
- Response Time Impact on Satisfaction  
- Heatmap of Low-rated Touchpoints  

### **4️⃣ Trend Analytics**
- Satisfaction Trends by Month  
- Seasonality Impact  
- Before vs After Service Improvements  

---

## 🛠️ Tools & Technologies  
- **Power BI**
- Data Cleaning in **Power Query**
- DAX Measures
- Data Modeling (Star Schema)

---

## 📊 DAX Highlights  
Some of the important DAX measures used in the dashboard:

```DAX
Average Satisfaction = AVERAGE(Survey[Rating])

Satisfied Customers = CALCULATE(COUNTROWS(Survey), Survey[Rating] >= 4)

Dissatisfied Customers = CALCULATE(COUNTROWS(Survey), Survey[Rating] <= 2)

NPS =
VAR Promoters = CALCULATE(COUNTROWS(Survey), Survey[Rating] >= 9)
VAR Detractors = CALCULATE(COUNTROWS(Survey), Survey[Rating] <= 6)
VAR Total = COUNTROWS(Survey)
RETURN (Promoters - Detractors) / Total

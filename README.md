# ✈️ Airline Data Management and Analysis Using Power BI

## 📌 Project Overview

The Airline Data Management and Analysis project is designed to analyze airline operations using Power BI. The project focuses on flight performance, passenger management, and ticket booking trends to provide meaningful business insights through interactive dashboards and visualizations.

This project demonstrates data cleaning, transformation, data modeling, DAX calculations, and dashboard development using Power BI.

---

## 🎯 Problem Statement

The airline industry manages large volumes of operational data related to flights, passengers, and ticket bookings. Efficient analysis of this data is essential for improving operational performance and customer satisfaction.

This project aims to transform raw airline data into actionable insights using Power BI.

---

## 🎯 Project Objectives

- Analyze flight operations and performance
- Monitor passenger distribution across airlines
- Track ticket booking status
- Identify best-performing flights
- Compare airline performance
- Build interactive dashboards
- Generate business insights for decision-making

---

## 📂 Datasets Used

### Flight Information

| Column Name |
|------------|
| FlightID |
| FlightNumber |
| Airline |
| Destination |
| Status |

### Passenger Information

| Column Name |
|------------|
| PassengerID |
| FlightID |
| SeatNumber |

### Ticket Information

| Column Name |
|------------|
| TicketID |
| FlightID |
| BookingStatus |

---

## 🧹 Data Preparation & Cleaning

Data cleaning and transformation were performed using Power Query.

### Steps Performed

- Removed duplicate records
- Removed blank rows
- Removed errors
- Changed data types
- Selected required columns
- Created conditional columns
- Extracted Flight Numbers using Column From Examples

---

## 🔗 Data Modeling

FlightID was used as the primary key to establish relationships between datasets.

### Relationships

- Flight Information (1) → Passenger Information (*)
- Flight Information (1) → Ticket Information (*)

### Cardinality

One-to-Many Relationship

---

## 📊 DAX Measures

### Total Flights

```DAX
Total Flights =
COUNT(flight_information[FlightID])
```

### Total Passengers

```DAX
Total Passengers =
COUNT(passenger_information[PassengerID])
```

### Total Tickets

```DAX
Total Tickets =
COUNT(ticket_information[TicketID])
```

### Best Flights

```DAX
Best Flights =
CALCULATE(
    COUNT(flight_information[FlightID]),
    flight_information[Custom] = "Best"
)
```

### Delayed Flights

```DAX
Delayed Flights =
CALCULATE(
    COUNT(flight_information[FlightID]),
    flight_information[Status] = "Delayed"
)
```

### Cancelled Flights

```DAX
Cancelled Flights =
CALCULATE(
    COUNT(flight_information[FlightID]),
    flight_information[Status] = "Cancelled"
)
```

---

## 📈 Dashboard Features

### KPI Cards

- Total Flights
- Total Passengers
- Total Tickets
- Best Flights
- Delayed Flights
- Cancelled Flights

### Visualizations

- Passenger Count by Airline
- Ticket Booking Status
- Flight Status Analysis
- Flights by Airline and Destination

### Interactive Features

- Airline Slicer
- Destination Slicer
- Flight Performance Slicer
- Interactive Navigation

---

## 📊 Project Results

| KPI | Value |
|------|------:|
| Total Flights | 200 |
| Total Passengers | 100 |
| Total Tickets | 50 |
| Best Flights | 82 |
| Delayed Flights | 58 |
| Cancelled Flights | 60 |

---

## 💡 Key Insights

- Airline D operates the highest number of flights (62).
- Airline A has the highest passenger count (30).
- Best Flights account for 82 flights.
- Delayed Flights account for 58 flights.
- Cancelled Flights account for 60 flights.
- Houston and Phoenix are major destinations.

---

## 🔒 Security Features

### Row Level Security (RLS)

Implemented RLS to restrict data access for Airline A users.

```DAX
[Airline] = "Airline A"
```

---

## 🛠️ Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Microsoft Excel

---

## 📷 Project Screenshots

### Dashboard

![Dashboard](Screenshots/Dashboard.png)

### Data Model

![Data Model](Screenshots/Data_Model.png)

### Airline Analysis

![Airline Analysis](Screenshots/Airline_Analysis.png)

### Insights

![Insights](Screenshots/Insights.png)

---

## 🚀 Business Impact

- Centralized airline data monitoring
- Improved operational visibility
- Better passenger and booking analysis
- Faster decision-making
- Interactive reporting experience

---

## 📁 Repository Structure

```text
Airline-Data-Management-and-Analysis-PowerBI
│
├── Data
│   ├── Flight_Information.xlsx
│   ├── Passenger_Information.xlsx
│   └── Ticket_Information.xlsx
│
├── Dashboard
│   └── Airline_Data_Management.pbix
│
├── Presentation
│   └── Airline_Data_Management_Presentation.pptx
│
├── Screenshots
│   ├── Dashboard.png
│   ├── Airline_Analysis.png
│   ├── Insights.png
│   ├── Data_Model.png
│   └── Power_Query_Cleaning.png
│
└── README.md
```

---

## 👨‍💻 Author

### Botta Lokesh

Aspiring Data Analyst | Power BI | SQL | Excel | Python

---

⭐ If you found this project useful, consider giving it a star.

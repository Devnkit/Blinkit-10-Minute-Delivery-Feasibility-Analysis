📦 Delivery Analysis 
---
🔍 Project Overview:

This project analyzes delivery time performance across multiple store locations in Delhi NCR. The primary goal is to evaluate the feasibility of a 10-minute delivery promise using spatial and statistical analysis.

I
Created a synthetic dataset of 100 delivery orders
Performed clustering and heatmapping to identify bottlenecks
Visualized store performance and demand zones

---

🧑‍💻 Technologies Used
Language: Python

Data Analysis: pandas, numpy

Visualization: matplotlib, seaborn, folium

ML/Clustering: scikit-learn (KMeans)

Geo Tools: geopy, scipy, googlemaps

---

📁 Dataset Description
The dataset was synthetically generated to simulate 100 delivery orders between July 15 and 21, 2024 from 5 fixed store locations.

Each record includes:

order_id, order_time, delivery_time

customer_lat, customer_lon

store_lat, store_lon

Computed fields:

duration (in minutes)

within_10min (Boolean: Was it delivered within 10 minutes?)

---

🛠️ Data Processing
Converted order_time and delivery_time to datetime.

Calculated duration in minutes.

Removed negative or null durations.

Added within_10min flag for success analysis.

---

📊 Visualizations
1. ✅ Delivery Time Distribution
Shows how many deliveries happened within specific time ranges.

2. 🌐 Delivery Result Map (Folium)
Mapped all customer delivery points:

🟢 Green = delivered within 10 minutes

🔴 Red = late deliveries

3. 🔵 Customer Clustering (KMeans)
Used KMeans clustering to divide customer locations into 5 delivery zones. Helps detect hotspots.

4. 📍 Store Performance Bubble Plot
Size of bubbles = number of orders
Text = average delivery duration

5. 📉 Average Delivery Time per Store
Shows comparison between stores’ delivery speeds.

6. 🔥 Customer Demand Heatmap
Visualizes where customers are concentrated using hexbin.

7. 📐 Voronoi Catchment Areas
Used Voronoi diagram to split the map into delivery zones based on store proximity.

8. 📊 Service Level Funnel
Displays how many deliveries occurred in:

≤10 mins

10–20 mins

20–30 mins

30 mins

9. ⚖️ Demand vs Speed (Scatter Plot)
Compares each store’s total orders vs average delivery duration.

---

📌 Key Insights
Only 30% of orders met the 10-minute delivery goal.

Cluster 1 had the highest delivery time (~15.6 mins).

Store at (28.6722, 77.4541) was the slowest.

Clustering helped identify overload zones.

---

🚀 Recommendations
Add fulfillment centers in dense clusters.

Implement real-time traffic routing.

Redistribute orders to nearby stores.

Introduce micro-warehouses or bike delivery units.

---

🔮 Future Scope
Integrate real delivery data from tracking apps.

Use Google Maps Directions API for ETA predictions.

Build a real-time dashboard using Streamlit or Dash.

Add time-series forecasting for demand planning.

---

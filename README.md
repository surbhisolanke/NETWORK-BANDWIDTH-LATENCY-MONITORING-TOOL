# NETWORK-BANDWIDTH-LATENCY-MONITORING-TOOL

📌 Project Overview

NetTrackers is a Python-based network monitoring project designed to measure and display network performance through a simple dashboard. The project measures network latency, download bandwidth, and upload bandwidth and stores the measurement results for further analysis.

The main purpose of the project is to measure important network performance parameters and present the results in an easy-to-understand format.

🎯 Current Features

The project includes a Streamlit dashboard with a simple sidebar-based interface. It contains separate sections for latency measurement, download bandwidth, upload bandwidth, continuous monitoring, and dashboard/reporting.

The Latency Measurement module measures the response time of selected network targets. The application uses two public DNS targets, 8.8.8.8 and 1.1.1.1. Five ping measurements are performed for each target. Each successful reading is displayed in a table, and the application calculates the average, minimum, and maximum latency.

The Download Bandwidth module measures the internet download speed using a speed test. The measured download speed is displayed in Mbps and stored in the SQLite database along with the measurement timestamp.

The Upload Bandwidth module measures the internet upload speed in Mbps. The result is displayed to the user and stored in the SQLite database with the corresponding timestamp.

The project stores network measurement data in an SQLite database. Latency readings contain information such as timestamp, target IP address, reading number, and latency value. Bandwidth measurements are stored with their measurement type, speed value, and timestamp.

A latency comparison feature is also available. After measuring both targets, the application calculates the average latency for 8.8.8.8 and 1.1.1.1 and displays the comparison using a bar graph. The application also indicates which target currently has the lower average latency.

🛠️ Technologies Used

Python – Main programming language

Streamlit – Dashboard and user interface

SQLite – Storage of latency and bandwidth readings

Pandas – Table and data handling

Matplotlib – Latency comparison graph

Speedtest – Download and upload bandwidth measurement

subprocess – Execution of the system ping command

Regular Expressions (re) – Extraction of latency values from ping output

datetime – Recording measurement timestamps

The interface is created using Streamlit components and does not require separate HTML, CSS, or JavaScript files.

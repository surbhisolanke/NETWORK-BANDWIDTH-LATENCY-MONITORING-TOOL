# NETWORK-BANDWIDTH-LATENCY-MONITORING-TOOL

📌 Project Overview
NetTrackers is a Python-based network monitoring project designed to measure and display network performance in a simple dashboard. The current version focuses on network latency measurement and provides the basic structure for future bandwidth measurement, continuous monitoring, and reporting features.

The main purpose of the project is to measure how quickly a network responds to a request. Latency is measured by sending ping requests to selected network targets and recording the response time in milliseconds. The current implementation uses two public DNS targets, 8.8.8.8 and 1.1.1.1, so their response times can be measured and compared.
🎯 Current Features
The project includes a Streamlit dashboard with a simple sidebar-based interface. It contains separate sections for latency measurement, download bandwidth, upload bandwidth, continuous monitoring, and dashboard/reporting.

The Latency Measurement module is currently implemented. When the user selects a target, the application performs five ping measurements. Each successful reading is displayed in a table with its reading number. The application also calculates and displays the average, minimum, and maximum latency.

The project stores individual latency readings in an SQLite database. Each stored record contains the timestamp, target IP address, reading number, and latency value. This database structure is intended to support future features such as network history, continuous monitoring, and report generation.

A comparison feature is also available. After measuring both targets, the application calculates the average latency for 8.8.8.8 and 1.1.1.1 and displays the results using a bar graph. The application also indicates which target currently has the lower average latency.
🛠️ Technologies Used
- Python – Main programming language
- Streamlit – Dashboard and user interface
- SQLite – Storage of latency readings
- Pandas – Table and data handling
- Matplotlib – Latency comparison graph
- subprocess – Execution of the system ping command
- Regular Expressions (re) – Extraction of latency values from ping output
- datetime – Recording measurement timestamps
The current interface is created using Streamlit components and does not require separate HTML, CSS, or JavaScript files.

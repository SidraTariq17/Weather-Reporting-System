# Weather Reporting System

This project is an **Integrated Environmental Monitoring System** implemented in C. It retrieves real-time environmental data (e.g., temperature, humidity) from the OpenWeatherMap API, processes the data, generates reports, and sends email alerts. The system is designed to be modular, efficient, and automated using shell scripts.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Repository Structure](#repository-structure)
3. [Features](#features)
4. [Libraries Used](#libraries-used)
5. [How to Use](#how-to-use)



---

## Project Overview

The system performs the following tasks:
1. **Data Retrieval**: Fetches real-time weather data from the OpenWeatherMap API.
2. **Data Processing**: Processes the raw data to calculate averages, detect anomalies, and generate insights.
3. **Report Generation**: Creates a text-based report from the processed data.
4. **Email Integration**: Sends email alerts with weather reports and notifications.
5. **Automation**: Uses shell scripts and cron jobs to automate data retrieval, processing, and report generation.

---

## Repository Structure
/Weather-Reporting-System
├── /src # Source code files
│ ├── main.c # Main program to fetch and process weather data
│ ├── email.c # Email functionality implementation
│ ├── headerfile1.c # Helper functions and utilities
│ └── mail.c # Script to send weekly weather reports
├── /include # Header files
│ ├── email.h # Declarations for email functionality
│ └── headerfile1.h # Constants, function prototypes, and includes
├── /scripts # Shell scripts for automation
│ ├── main.sh # Script to run the main program
│ └── mail.sh # Script to automate email sending
├── /data # Data files
│ ├── api_response.json # Raw API response from OpenWeatherMap
│ ├── processed_data.json # Processed weather data
│ └── report_generating.txt # Generated weather report
├── Makefile # Makefile for building the project


---

## Features

- **Real-Time Data Retrieval**: Fetches weather data from the OpenWeatherMap API.
- **Data Processing**: Calculates averages, detects anomalies, and generates insights.
- **Report Generation**: Creates a text-based report for easy readability.
- **Email Alerts**: Sends email notifications with weather reports and alerts.
- **Automation**: Uses shell scripts and cron jobs for scheduled tasks.
- **Modular Design**: Organized into reusable modules for better maintainability.
- **Error Handling**: Includes basic error handling for file operations and API requests.

---

## Libraries Used

- **cURL**: For making HTTP requests to the OpenWeatherMap API.
- **cJSON**: For parsing and generating JSON data.
- **Standard C Libraries**: For file handling, memory management, and string manipulation.
- **Linux System Calls**: For desktop notifications and automation.

---

## How to Use

### Prerequisites
- Install `libcurl` and `cJSON` libraries.
- Obtain an API key from [OpenWeatherMap](https://openweathermap.org/api).

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Weather-Reporting-System.git
   cd Weather-Reporting-System
Update the API key in the source code (replace YOUR_API_KEY in main.c).

Build the project using the Makefile:

bash
Copy
make
Run the main program:

bash
Copy
./main
Automate tasks using the provided shell scripts:

Run main.sh to fetch and process data daily.

Run mail.sh to send weekly weather reports.

Automation with Cron
Add the following lines to your crontab:

bash
Copy
35 19 * * * /path/to/Weather-Reporting-System/scripts/main.sh
0 8 * * 1 /path/to/Weather-Reporting-System/scripts/mail.sh
This will:

Run main.sh daily at 7:35 PM to fetch and process data.

Run mail.sh every Monday at 8:00 AM to send the weekly report.

Future Expansions
User Interface (UI): Develop a graphical or web-based interface for better user interaction.

Location-Based Forecast: Allow users to input location coordinates dynamically.

Enhanced Reporting: Include graphical representations like charts and graphs.

Mobile Application: Develop a mobile app for push notifications.

Integration with External Services: Integrate with calendar or task management tools.


This `README.md` provides a comprehensive overview of the project, its structure, features, and usage instructions. It is designed to help users understand and use the repository effectively.


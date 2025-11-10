
# Weather Data Pipeline with Airflow

This project is a complete data pipeline that collects daily weather information for cities using the OpenWeatherMap API. The data is automatically extracted, processed, and stored in a PostgreSQL database through Apache Airflow, and then visualized with Metabase. All components run in a fully containerized environment using Docker Compose.


## Technology Stack

- Apache Airflow – workflow orchestration and automation  
- PostgreSQL – database for structured data storage  
- Docker Compose – containerized infrastructure setup  
- Metabase – visualization and dashboarding tool  
- pgAdmin – graphical database management interface  


## Architecture

The system runs on Docker and is composed of several services that interact with each other. Airflow retrieves data from the OpenWeatherMap API, transforms the raw JSON response, and loads the cleaned data into PostgreSQL. Metabase then connects to the database to generate charts and dashboards.


## Setup Instructions

1. Clone the Repository
   git clone https://github.com/LanaSmit/Pipeline_Airflow_Docker_Metabase.git
   cd weather-data-pipeline

2. Configure Environment Variables

   Create your .env file
   Then open the .env file:
   Set your own database username and password.
   Add your OpenWeather API key.
   You can obtain an API key by creating an account on the OpenWeather website

3. Start the Services

   Run the following command to build and start all containers:
   docker compose up --build

4. Access the Applications

   Once everything is running, open the following in your browser:

   Airflow: http://localhost:8080

   pgAdmin: http://localhost:5050
   
   Metabase: http://localhost:3000

   Use the credentials defined in your .env file to log in.

5. Run and Explore

   Use Airflow to trigger and monitor your DAGs.
   Use pgAdmin to view and query your PostgreSQL database.
   Use Metabase to visualize and analyze the processed data.

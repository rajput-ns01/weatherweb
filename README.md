Weather Forecast Application
This application is a Java servlet that fetches current weather data for a specified city using the OpenWeatherMap API and displays it in a JSP page.

Features
User can input a city name to get real-time weather data.
The application retrieves and displays:
Current temperature (in Celsius)
Humidity
Wind speed
Weather condition
Date and time of the report
Technologies Used
Java (Servlet)
Jakarta Servlet API
OpenWeatherMap API
Google Gson (for JSON parsing)
JSP (JavaServer Pages)
Prerequisites
Java 11+
Apache Tomcat or any other Java servlet container
OpenWeatherMap API key (sign up at OpenWeatherMap if you don't have one)
Setup Instructions
Clone the repository:

bash
cd weather
Configure OpenWeatherMap API Key: In MyServlet.java, replace the existing API key with your own:

java
String apiKey = "YOUR_API_KEY";
Build and deploy the application:

Add the project to your favorite IDE.
Ensure Tomcat is installed and configured with your IDE.
Run the project on the server.
Access the application:

Go to http://localhost:8080/YourAppName/MyServlet in your browser.
Usage
Enter the city name in the input field and submit the form.
The servlet will fetch data from the OpenWeatherMap API for the specified city and display it on the JSP page.
Code Explanation
MyServlet class (Java Servlet)
API Connection: Sends a GET request to OpenWeatherMap API to fetch weather data for the provided city.
JSON Parsing: Uses Gson to parse the API response and extract weather details.
Attributes Setting: Sets attributes with the parsed weather data to be used in the JSP page.
JSP Forwarding: Forwards the request to index.jsp to display the weather details.
index.jsp (JSP Page)
Displays the weather data (temperature, humidity, wind speed, etc.) fetched from the servlet.
Sample Output
City: Paris
Temperature: 25°C
Weather Condition: Clear
Humidity: 40%
Wind Speed: 5.0 m/s
Date and Time: 2024-10-25
Dependencies
Ensure the following dependencies are in your classpath (e.g., via Maven):

jakarta.servlet-api
gson

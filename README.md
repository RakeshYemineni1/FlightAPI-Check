# FlightAPI-Check ✈️

This project demonstrates how to make API calls to the **aviationstack** API using Java. It fetches flight information, parses the JSON response, and maps it to Java objects for easy access and manipulation.

---

### 🚀 Getting Started

To get this project running on your local machine, follow these steps.

#### Prerequisites

* **Java Development Kit (JDK)**: Version 17 or higher.
* **Maven**: To manage project dependencies.
* **Aviationstack API Key**: You need to register on the aviationstack website and obtain an API key.

#### Installation

1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/RakeshYemineni1/FlightAPI-Check.git](https://github.com/RakeshYemineni1/FlightAPI-Check.git)
    cd FlightAPI-Check
    ```
2.  **Configure your API key**: Open the `Main.java` file and replace `"YOUR_REAL_API_KEY"` with your actual aviationstack API key.
    ```java
    String apiKey = "YOUR_REAL_API_KEY";
    ```
3.  **Build the project**: Use Maven to download dependencies and build the project.
    ```bash
    mvn clean install
    ```

---

### 📖 How it Works

The project uses the `java.net.http.HttpClient` to make an HTTP GET request to the aviationstack API. The API key is passed as a query parameter in the URL for authentication.

The core functionality includes:
* **API Request**: A request is sent to the `https://api.aviationstack.com/v1/flights` endpoint.
* **JSON Parsing**: The response is a JSON string. The project uses the **Gson** library to parse this string and automatically map it to a set of custom Java classes (`ApiResponse`, `Flight`, `AirportInfo`, etc.).
* **Data Handling**: The parsed data is then accessed from the Java objects, allowing for clean and simple extraction of flight details such as flight number, status, and airport information.

---

### ⚙️ Project Structure

* `src/main/java/org/example/Main.java`: The main class containing the logic for the API call and data processing.
* `src/main/java/org/example/*.java`: Java classes (`ApiResponse`, `Flight`, etc.) that model the JSON response structure.
* `pom.xml`: The Maven configuration file, which includes the Gson dependency.

---

### 📝 Example Output

A successful run of the application will print output similar to this:

API call was successful!
Flight Number: 1004
Flight Status: active
Departure IATA: SFO
Departure Airport: San Francisco International

# Exercise 11 - API Integration and Data Processing

| Section | Description |
| :--- | :--- |
| **Aim** | [cite_start]Call a REST API (Ex. Weather API), process the JSON response, and write the data to a database[cite: 504]. |
| **Tool** | UiPath Studio with the **`UiPath.WebAPI.Activities`** and **`UiPath.Database.Activities`** packages installed. |

---

## Aim

The objective is to connect to an external service (Weather API) via its REST API, extract specific data points (Temperature, Humidity) from the JSON payload, and persist this extracted information into a structured database[cite: 504].

## Procedure

1.  **Install Activities:** Install the **`UiPath.WebAPI.Activities`** package[cite: 513].
2.  **HTTP Request:** Use the **`HTTP Request`** activity set to the `GET` method[cite: 519]. [cite_start]The Request URL is constructed using the WeatherAPI endpoint, the `apiKey` variable, and the user-provided `city` variable[cite: 520].
3.  **Process JSON:** Use the **`Deserialize JSON`** activity to convert the HTTP response content into a `JObject`[cite: 522, 523].
4.  **Extract Data:** Use **`Assign`** activities with expressions like `json("main")("temp").ToString` to extract required values (e.g., temperature and humidity) from the JSON structure.

## Output

* **Input:** The Weather API provides weather data (e.g., temperature, humidity) in JSON format.
  <img width="1919" height="1048" alt="image" src="https://github.com/user-attachments/assets/063ee9e6-3229-4586-b445-9a5dda74ff60" />

* **Output:** The extracted data is successfully displayed.
  <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/534c0797-7dc2-4387-992e-19651e4f38a2" />


## Result

The automation successfully integrated with a third-party REST API, parsed the resulting JSON, and inserted the required data points into a database, demonstrating a complete API integration workflow[cite: 531].

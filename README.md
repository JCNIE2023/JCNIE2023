 <!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.lordicon.com/lordicon.js"></script>

    <title>Weather Update - Iligan City</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        background-color: hsl(208, 78%, 79%);
        color: #232323;
        text-align: center;
        font-size: 1.5em;
        padding:80px;
      }
      #weather {
        margin-top: 20px;
        padding: 20px;
        background-color: #ffffff;
        border-radius: 5px;
        box-shadow: 0 0 10px rgba(175, 173, 173, 0.1);
        display: inline-block;
        border-style: solid;
        font-size: 1em;
        border-radius: 20%;
      }
p{
    font-size: 1em;
}
      footer{ 
      padding: 10px;
      padding-left: 10px;
 
     
    display: center;
    border-style: inset;
    border-radius: 20%;
    border-color: black;
      }
     
    </style>



   
  <body>
    <h1>Weather Update - Iligan City</h1>

    <div id="weather">
      <p>Loading weather data...</p>
    </div>

<div id ="update">
    <H1>Weather Information:</H1>
    <p>The average temperature in Iligan in August for a typical day ranges from a high of 81°F (27°C) to a low of 72°F
        (22°C). Some would describe it as pleasantly warm with a gentle breeze.

        For comparison, the hottest month in Iligan, April, has days with highs of 87°F (30°C) and lows of 74°F (23°C).
        The coldest month, February has days with highs of 82°F (28°C) and lows of 71°F (21°C). This graph shows how an
        average day looks like in Iligan in Agust based on historical data.</p>
<br>
    <h1>Humidity</h1> 
    </lord-icon>
    <li>Humidity: 90% </li>
    <li>Wind: 8 km/h WeatherWednesday 2:00 PMRain</li>
    <br>
    <table>
        <thead>
            <th><lord-icon
                    src="https://cdn.lordicon.com/zawvkqfy.json"
                    trigger="hover"
                    stroke="bold"
                    style="width:25px;height:20px">
                </lord-icon>MONDAY</th>
            
            <th><lord-icon
                    src="https://cdn.lordicon.com/zawvkqfy.json"
                    trigger="hover"
                    stroke="bold"
                    style="width:25px;height:20px">
                </lord-icon>TUESDAY</th>
            <th><lord-icon
                    src="https://cdn.lordicon.com/zawvkqfy.json"
                    trigger="hover"
                    stroke="bold"
                    style="width:25px;height:20px">
                </lord-icon>WENDSDAY</th>
            <th><lord-icon
                    src="https://cdn.lordicon.com/zawvkqfy.json"
                    trigger="hover"
                    stroke="bold"
                    style="width:25px;height:20px">
                </lord-icon>THURSDAY</th>
            <th><lord-icon
                    src="https://cdn.lordicon.com/zawvkqfy.json"
                    trigger="hover"
                    stroke="bold"
                    style="width:25px;height:20px">
                </lord-icon>FRIDAY</th>
            <th><lord-icon
                    src="https://cdn.lordicon.com/zawvkqfy.json"
                    trigger="hover"
                    stroke="bold"
                    style="width:25px;height:20px">
                </lord-icon>SATURDAY</th>
            <th><lord-icon
                    src="https://cdn.lordicon.com/zawvkqfy.json"
                    trigger="hover"
                    stroke="bold"
                    style="width:25px;height:20px">
                </lord-icon>SUNDAY</th>
            <tr>
                <td>Hourly Weather · 1 PM 90°. rain drop 49% · 2 PM 89°. rain drop 51% · 3 PM 88°. rain drop 56% · 4 PM
                    86°. rain drop 27% · 5 PM 85°. rain drop 22% · 6 PM 83°.</td>

                <td>Hourly Weather · 1 PM 90°. rain drop 49% · 2 PM 89°. rain drop 51% · 3 PM 88°. rain drop 56% · 4 PM
                    86°. rain drop 27% · 5 PM 85°. rain drop 22% · 6 PM 83°.</td>

                <td>Hourly Weather · 1 PM 90°. rain drop 49% · 2 PM 89°. rain drop 51% · 3 PM 88°. rain drop 56% · 4 PM
                    86°. rain drop 27% · 5 PM 85°. rain drop 22% · 6 PM 83°.</td>

                <td>Hourly Weather · 1 PM 90°. rain drop 49% · 2 PM 89°. rain drop 51% · 3 PM 88°. rain drop 56% · 4 PM
                    86°. rain drop 27% · 5 PM 85°. rain drop 22% · 6 PM 83°.</td>

                <td>Hourly Weather · 1 PM 90°. rain drop 49% · 2 PM 89°. rain drop 51% · 3 PM 88°. rain drop 56% · 4 PM
                    86°. rain drop 27% · 5 PM 85°. rain drop 22% · 6 PM 83°.</td>

                <td>Hourly Weather · 1 PM 90°. rain drop 49% · 2 PM 89°. rain drop 51% · 3 PM 88°. rain drop 56% · 4 PM
                    86°. rain drop 27% · 5 PM 85°. rain drop 22% · 6 PM 83°.</td>

                <td>Hourly Weather · 1 PM 90°. rain drop 49% · 2 PM 89°. rain drop 51% · 3 PM 88°. rain drop 56% · 4 PM
                    86°. rain drop 27% · 5 PM 85°. rain drop 22% · 6 PM 83°.</td>
            </tr>
        </thead>
    </table>
<br>
</div>



    <script>
      document.addEventListener("DOMContentLoaded", async function () {
        const apiKey = "cc68bd4d6b26495ba2d60337241208";
        const cityName = "Iligan";
        const apiEndpoint = https//api.weatherapi.com/v1/forecast.json?key=${apiKey}&q=${cityName};
      
        try {
          const response = await fetch(apiEndpoint); // Wait for the fetch to complete
          const weatherData = await response.json(); // Wait for the response to be parsed into JSON
          console.log(weatherData);

          const weatherContainer = document.getElementById("weather");
          const temperatureInCelsius = weatherData.current.temp_c;
          const weatherDescription = weatherData.current.condition.text;
          const humidityLevel = weatherData.current.humidity;

          weatherContainer.innerHTML = `
           <h2>${cityName}</h2>
           <p><strong>Temperature:</strong> ${temperatureInCelsius}°C</p>
           <p><strong>Weather:</strong> ${weatherDescription}</p>
           <p><strong>Humidity:</strong> ${humidityLevel}%</p>
       `;
        } catch (error) {
          const weatherContainer = document.getElementById("weather");
          weatherContainer.innerHTML = <p>Unable to retrieve weather data: ${error.message}</p>;
        }
      });
    </script>
  </body>

  <br>
  <footer>JC NIEL KINGS. PEJE 08/14/2024 </footer>


</html>

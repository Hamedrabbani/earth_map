# earth_map
Global Earthquake Visualization with Plotly

This project uses data from a local JSON file containing earthquake records
and plots them on an interactive world map using Plotly's scattergeo chart type.
The earthquakes are visualized geographically with marker sizes and colors reflecting their magnitudes.

Features:
•	Loads and parses a GeoJSON dataset of earthquake events
•	Extracts latitude, longitude, magnitude, and summary information
•	Visualizes all events on an interactive world map
•	Marker size is scaled to reflect earthquake magnitude
•	Hovering over a marker displays descriptive information (location, magnitude)
•	Automatically generates and opens an HTML file (global_earthquakes.html)

File Structure:
•	earth.json – Local GeoJSON dataset (must follow USGS-style earthquake feed)
•	main.py – The script that processes the JSON data and builds the visualization
•	global_earthquakes.html – Output interactive map generated with Plotly.

Technologies Used:
•	Python 3.x
•	json module – For reading and parsing the GeoJSON file
•	Plotly (plotly.graph_objs and plotly.offline) – For creating the geographic visualization

How to Run:
1.	Make sure you have Python installed.
2.	Install Plotly if you haven’t already

pip install plotly 

1.	Place your earthquake dataset (earth.json) in the same directory as your script.
2.	Run the script:

earth_map.py
1.	Your default web browser will open a file named global_earthquakes.html showing the map.

Notes:
o	The earthquake magnitudes (mag) are multiplied by 5 to scale marker sizes for better visibility.
o	The colorscale used is "ice", but you can explore others like "Viridis", "Hot", or "Jet" to customize the look.
o	This project assumes the input data structure matches the standard USGS GeoJSON format (features
array with propertiesand geometry).

Example Output

Each point on the map:
o	Appears at its correct geographic location
o	Has a size proportional to the strength of the earthquake
o	Shows a tooltip on hover with details like magnitude and title


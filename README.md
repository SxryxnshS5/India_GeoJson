# India GeoJSON Map  

This repository contains a **GeoJSON file of India's map**, including detailed state and territory boundaries. The map is designed for use in applications requiring accurate geographical representations of India.  

**Repository URL:** [India_GeoJson](https://github.com/SxryxnshS5/India_GeoJson)  

---

## Key Features  
- **Comprehensive representation of India's geographical boundaries:**  
  - Includes **Jammu & Kashmir**, along with **Pakistan-occupied Kashmir (POK)** and **Aksai Chin** as part of the state.  

## Current Limitations  
- **Telangana Missing:**  
  - The current map does not include the state of **Telangana**.  
  - Telangana will be added soon in an upcoming update, so stay tuned!  

## File Details  
- **`IndiaGeoJson.geojson`:**  
  The GeoJSON file representing India's map with state boundaries and detailed geometry.  

## Usage  
This GeoJSON file can be used in:  
- Web mapping applications.  
- Data visualization projects.  
- GIS software for spatial analysis.  

### Example Integration  
Here’s a quick example of how to use the GeoJSON file with [Leaflet](https://leafletjs.com):  
```javascript
var map = L.map('map').setView([20.5937, 78.9629], 5);

L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png').addTo(map);

fetch('india_map.geojson')
  .then(response => response.json())
  .then(data => {
    L.geoJSON(data).addTo(map);
  });
```  

## Planned Updates  
- Adding Telangana as a separate state.  
- Inclusion of metadata for each state (e.g., names, population, etc.) to enable interactive features.  

## Contributing  
Contributions are welcome! If you would like to:  
- Fix any issues in the map.  
- Enhance the map with missing details (like Telangana) or additional metadata.  

Feel free to fork the repository, make changes, and submit a pull request.  

## License  
This project is licensed under the [MIT License](LICENSE).  

## Disclaimer  
This GeoJSON map reflects the geographical boundaries of India as per the author’s perspective, including regions like **POK** and **Aksai Chin** as part of India. Please note that the representation may include territories whose status is subject to international disputes.  
This map is for general-purpose use and should not be considered an authoritative reference.  

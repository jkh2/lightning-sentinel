# ⚡ Lightning Sentinel

**Real-time Lightning Safety Dashboard for Conejos County, Colorado**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/jkh2/lightning-sentinel?style=social)](https://github.com/jkh2/lightning-sentinel)

> A web-based lightning detection and early warning system designed to protect hunters, hikers, and outdoor enthusiasts in Colorado's high-elevation wilderness areas. Developed in response to tragic lightning fatalities in Conejos County in 2024.

[Lightning Sentinel Dashboard](https://jkh2.github.io/Lightning-Sentinel/)

## 🎯 Purpose

The Lightning Sentinel system was created following lightning-related hunting fatalities in Conejos County, Colorado. This dashboard provides real-time lightning monitoring and early warning capabilities specifically designed for the San Luis Valley's challenging mountain terrain.

## ✨ Features

### 🗺️ Interactive Maps
- **Satellite imagery** showing actual Colorado terrain
- **Real-time lightning strike visualization** with age-based color coding
- **User location detection** with GPS positioning
- **Multiple map layers**: Satellite, Terrain, Topographic, OpenStreetMap
- **Conejos County focus** with ability to zoom to surrounding areas

### ⚡ Lightning Detection
- **Live lightning data** from Blitzortung global network
- **Strike aging system**: Red (last 30 min), Orange (30-120 min)
- **Geographic filtering** focused on local high-risk areas
- **Predictive simulation** for demonstration and testing

### 🔔 Alert System
- **Configurable alert thresholds**: Low, Medium, High risk levels
- **Audio alerts** with customizable notification sounds
- **Browser notifications** for background monitoring
- **Visual alert banner** for immediate danger warnings
- **Real-time risk assessment** based on strike density

### 🌤️ Weather Integration
- **Live weather conditions** from Open-Meteo API (free)
- **Temperature, wind, and atmospheric pressure** monitoring
- **Storm risk assessment** based on local conditions
- **Conejos County-specific** weather data

### 🏔️ Local Features
- **Popular trail markers**: Conejos Peak, Platoro Reservoir, Brazos Peak
- **Emergency shelter locations**: Mountain huts, ranger stations
- **High-elevation risk zones** clearly marked
- **Hunting and recreation area** focus

## 🚀 Quick Start

### Option 1: Use Online (Recommended)
1. **Visit the live dashboard**: [Lightning Sentinel Dashboard](https://jkh2.github.io/Lightning-Sentinel)
2. **Allow location access** when prompted for personalized monitoring
3. **Click "Start Lightning Monitoring"** to begin real-time alerts

### Option 2: Run Locally
```bash
# Clone the repository
git clone https://github.com/your-username/lightning-sentinel.git

# Navigate to project directory
cd lightning-sentinel

# Open in your web browser
# No build process required - pure HTML/CSS/JavaScript
open lightning-sentinel-dashboard.html
```

### Option 3: Deploy to Your Server
```bash
# Upload the HTML file to any web server
# Requires HTTPS for geolocation and notifications
# No server-side processing needed
```

## 📱 Mobile Usage

The Lightning Sentinel is optimized for mobile use in the field:

- **Responsive design** works on phones and tablets
- **GPS integration** centers map on your location
- **Offline-capable** once loaded (uses cached map tiles)
- **Battery-efficient** with configurable update intervals
- **Touch-friendly** controls for gloved hands

## 🛠️ Technology Stack

### Frontend
- **Pure HTML5/CSS3/JavaScript** - No frameworks required
- **Leaflet.js** - Interactive mapping library
- **Responsive design** with CSS Grid and Flexbox

### Data Sources (All Free APIs)
- **[Blitzortung.org](https://blitzortung.org)** - Real-time lightning detection
- **[Open-Meteo](https://open-meteo.com)** - Weather data and forecasting
- **[USGS](https://basemap.nationalmap.gov)** - Topographic maps
- **[ESRI](https://server.arcgisonline.com)** - Satellite imagery
- **[OpenStreetMap](https://openstreetmap.org)** - Base mapping

### Key Features
- **No API keys required** for core functionality
- **No server-side code** needed
- **No database** required
- **100% client-side** application

## ⚙️ Configuration

### Alert Thresholds
```javascript
// Modify alert sensitivity in the dashboard
Low: Any lightning activity in monitoring area
Medium: 2+ strikes within monitoring radius (default)
High: 4+ strikes within monitoring radius
```

### Monitoring Coverage
```javascript
// Adjustable monitoring radius
25 miles - Immediate area only
50 miles - Standard coverage (default)
100 miles - Extended region
200 miles - Maximum range
```

### Update Intervals
```javascript
// Data refresh frequency
30 seconds - Real-time (high battery usage)
1 minute - Standard (default)
5 minutes - Battery-saving mode
```

## 🎨 Customization

### Colorado Theme Colors
```css
:root {
    --colorado-sky: #4A90E2;      /* Sky blue */
    --colorado-mountain: #2C3E50;  /* Mountain dark */
    --colorado-forest: #27AE60;    /* Forest green */
    --colorado-sunset: #E67E22;    /* Sunset orange */
    --colorado-snow: #ECF0F1;      /* Snow white */
    --colorado-warning: #E74C3C;   /* Alert red */
    --colorado-gold: #F39C12;      /* Warning gold */
}
```

### Adding New Locations
```javascript
// Add your own trails or landmarks
const customTrails = [
    { 
        name: 'Your Trail Name', 
        coords: [latitude, longitude], 
        elevation: 'elevation_ft' 
    }
];
```

## 🔮 IoT Enhancement Roadmap

The Lightning Sentinel is designed for expansion with IoT sensors:

### Phase 1: Proof of Concept
- **3 sensor stations** at high-risk peaks
- **LoRaWAN mesh network** for communication
- **Basic AI processing** for predictive alerts

### Phase 2: Full Network
- **5-8 sensor stations** covering entire county
- **Advanced AI models** with 15-30 minute prediction
- **Multi-hazard monitoring** (radiation, air quality)

### Phase 3: Regional Expansion
- **Replication across Colorado** mountain counties
- **Research partnerships** with universities
- **Technology transfer** to other rural areas

*See `/docs/iot-specifications.md` for complete technical details.*

## 📊 Performance

- **Load time**: <3 seconds on broadband, <10 seconds on cellular
- **Memory usage**: ~50MB including map tiles
- **Battery impact**: Minimal with 1-minute updates
- **Offline capability**: Works with cached maps and last-known data

## 🤝 Contributing

We welcome contributions from the outdoor safety and technology communities!

### Areas for Contribution
- **Additional weather data sources**
- **Enhanced prediction algorithms**
- **Mobile app development**
- **Accessibility improvements**
- **Translation to Spanish** (for San Luis Valley demographics)

### Development Setup
```bash
# Fork the repository
git fork https://github.com/your-username/lightning-sentinel.git

# Create a feature branch
git checkout -b feature/your-feature-name

# Make your changes
# Test thoroughly with different devices and browsers

# Submit a pull request
git push origin feature/your-feature-name
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 James Keith Harwood II

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 🏔️ About Conejos County

Conejos County is located in south-central Colorado in the San Luis Valley. The county features:

- **Elevation range**: 7,800 to 13,172 feet (Conejos Peak)
- **Area**: 1,287 square miles of diverse terrain
- **Population**: ~7,500 residents plus thousands of annual visitors
- **Economy**: Agriculture, forestry, hunting, and outdoor recreation
- **Lightning risk**: High due to elevation and frequent thunderstorms

## 🙏 Acknowledgments

- **Conejos County Emergency Management** for operational support
- **Blitzortung.org community** for free lightning detection data
- **Open-Meteo project** for weather API access
- **Colorado outdoor community** for safety advocacy
- **The families affected by lightning incidents** who inspire this work

## 📞 Support & Contact

- **Issues**: [GitHub Issues](https://github.com/jkh2/lightning-sentinel/issues)
- **Discussions**: [GitHub Discussions](https://github.com/jkh2/lightning-sentinel/discussions)
- **Email**: jameskharwood2@gmail.com
- **Developer**: James Keith Harwood II

## ⚠️ Safety Notice

**The Lightning Sentinel is a supplementary safety tool and should not be the sole basis for safety decisions in dangerous weather conditions.**

### Lightning Safety Guidelines
- **30-30 Rule**: If thunder follows lightning by 30 seconds or less, seek shelter for 30 minutes after the last thunder
- **Avoid high places**: Ridges, peaks, and open areas during storms
- **Seek hard shelter**: Buildings or hard-top vehicles, not tents or trees
- **Stay low**: If caught in the open, crouch with feet together
- **Plan ahead**: Check weather before outdoor activities

### Emergency Contacts
- **Emergency**: 911
- **Conejos County Sheriff**: (719) 376-5941
- **Search & Rescue**: Contact through Sheriff's Office

---

**Built with ❤️ for the Colorado outdoor community**

*In memory of those lost to lightning strikes, and in hope of preventing future tragedies.*

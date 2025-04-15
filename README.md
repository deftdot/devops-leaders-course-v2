# Devops Leaders IL Course - Test App
This project is a Python web application built with FastAPI that displays the latest weather reports for a user-specified location along with an interactive map using Leaflet.js. The project uses Bootstrap for styling and features enhanced CSS to provide a modern and responsive user interface.
The Project was built with the assistance of OpenAI o3-mini-high model.


## Features

- **Weather Reports:** Get the latest weather information by entering a location.
- **Interactive Map:** Displays the location on an interactive map.
- **Enhanced UI:** Modern and responsive design using Bootstrap and custom CSS.
- **API Integration:** Uses the [wttr.in API](https://wttr.in/) to fetch weather details.

## Getting Started

### Prerequisites

- Python 3.8 or higher

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/deftdot/devops-leaders-course-v2.git
cd weather-map-dashboard
```

2. **Create a virtual environment (optional, but recommended):**
```bash
python -m venv venv  
source venv/bin/activate  # On Windows: .\venv\Scripts\activate  
```

3. **Install the required packages:**
```bash
pip install -r requirements.txt  
```

### Running the Application

**Run the FastAPI server using Uvicorn:**
```bash
uvicorn main:app --reload 
```
**Open your browser and navigate to:**
```bash
http://127.0.0.1:8000
```

## Stress Test Configuration and Cautions

The CPU stress test feature in this application is protected by a feature flag. To enable the CPU stress test functionality, set the environment variable **STRESS_TEST_FLAG** to `"true"` (case‑insensitive). If this flag is missing, empty, or set to any other value, the stress test endpoints and UI section will be disabled.

### Configuration Options

- **Duration:**  
  Specify the total runtime (in seconds) for the CPU stress test via the "Duration (sec)" input.

- **Load:**  
  Set the desired CPU load percentage (0–100) using the slider.  
  **Note:** A load value above 50% will trigger a confirmation popup, warning that high CPU loads may heavily overburden your system.

### Caution

- **High CPU Load:**  
  Running the CPU stress test can significantly load your CPU across all cores, potentially degrading system performance or causing temporary unresponsiveness. Use this feature only in a controlled test environment.

- **Multiprocessing:**  
  The application employs multiprocessing to distribute the stress across all available CPU cores. Monitor your system’s resource usage accordingly to avoid unintended impacts.

- **Feature Flag:**  
  Ensure that you understand the implications of enabling the stress test. It is recommended to leave the **STRESS_TEST_FLAG** disabled (or set to any value other than `"true"`) during normal operation.

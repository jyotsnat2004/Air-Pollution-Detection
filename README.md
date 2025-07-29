# Air Pollution Detection Using Computer Vision and Sensor Data

This project analyzes air pollution using both sensor data and image processing techniques. It leverages Python libraries to process CSV sensor data, visualize trends, and detect pollution in images using computer vision.

## Features
- Reads and analyzes air quality sensor data from CSV files
- Visualizes temperature, humidity, and air quality trends over time
- Detects pollution (haze/smoke) in images using OpenCV (contrast, brightness, edge detection, color analysis)
- Classifies air quality based on computed pollution score

## Requirements
- Python 3.x
- pandas
- matplotlib
- seaborn
- opencv-python
- numpy

## Installation
1. Clone or download this repository.
2. Install the required Python packages:
   ```bash
   pip install pandas matplotlib seaborn opencv-python numpy
   ```
3. Place your sensor data CSV (e.g., `test.csv`) and images (e.g., `clearSKY.jpeg`, `polluted.jpeg`) in the working directory.

## Usage
### 1. Sensor Data Analysis
- The notebook reads sensor data from a CSV file (e.g., `test.csv`).
- It visualizes temperature, humidity, and air quality sensor readings over time using matplotlib.

### 2. Image-Based Pollution Detection
- The function `detect_pollution(image_path)` analyzes an image to estimate pollution:
  - Computes contrast, brightness, edge density, blue channel intensity, and saturation.
  - Classifies the image as sky or landscape and calculates a pollution score.
  - Displays the original image and edge detection result.
  - Outputs a pollution score (higher = more polluted) and a qualitative air quality label.
- Example usage:
  ```python
  detect_pollution('clearSKY.jpeg')
  detect_pollution('polluted.jpeg')
  ```

## Example Output
- Pollution Score: 42.7/100 (Good, Clean Air)
- Pollution Score: 94.7/100 (Poor, Heavy Pollution)

## Notes
- Adjust thresholds in `detect_pollution` as needed for your dataset and images.
- For questions or support, contact: vatshayan007@gmail.com

## License
This project is for educational and research purposes only. 

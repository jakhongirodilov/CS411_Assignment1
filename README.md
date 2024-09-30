# Human Activity Recognition - Data Processing and Machine Learning Pipeline

## Project Overview
This project processes accelerometer data from multiple participants to classify human activities. The dataset contains readings from sensors attached to the back and thigh, recording movement in free-living settings. The goal is to clean, transform, and build a machine learning model to recognize different activities.

## Dataset
The dataset used in this project is not included directly in the repository. You can download it from the following link:
- [HARTH Dataset Download Link](https://archive.ics.uci.edu/dataset/779/harth)

The dataset contains:
- **Timestamp**: Date and time of each reading.
- **back_x, back_y, back_z**: Accelerometer data from the back sensor.
- **thigh_x, thigh_y, thigh_z**: Accelerometer data from the thigh sensor.
- **label**: Activity labels.

## Steps
1. **Data Loading**: Download the dataset and place it in a folder named `harth`. The script will combine multiple CSV files into a single dataset.
2. **Data Cleansing**: Removed duplicates and filtered data within a valid range (-3g to +3g).
3. **Feature Engineering**: 
   - Extracted hour, minute, and second from timestamps.
   - Calculated movement magnitude for back and thigh sensors.
4. **Data Normalization**: Applied Min-Max scaling to sensor data.
5. **Model Training**: Split data into train/test sets and used a Random Forest model to classify activities.

## Requirements
- Python 3.x
- Libraries: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

## How to Run
1. Clone the repository.
2. Install dependencies using the following command:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the dataset from the link above and place it in a folder named `harth`. Your folder structure should look like this:

   ```bash
   /YourProjectFolder
   ├── visualizations         # file containing visualization images
   ├── assignment1.ipynb      # Jupyter Notebook with the data processing and model
   ├── requirements.txt       # File with Python package dependencies
   ├── README.md              # Project documentation
   └── harth/                 # Folder containing the dataset (to be created by user)
       ├── S008.csv
       ├── S009.csv
       ├── S010.csv
       ├── S013.csv
       ├── S015.csv
       ├── ...
   ```

4. Run the Jupyter Notebook (`assignment1.ipynb`) to process the dataset and train the model.
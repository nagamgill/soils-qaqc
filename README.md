Soil Data Analysis

This Jupyter notebook is dedicated to the analysis of soil moisture and temperature data from the DMP Arapahoe Ridge site. It includes data loading, preprocessing, visualization, and normalization steps. The code also implements various methods for cleaning the data, such as spike removal and applying a rolling median filter. Additionally, the notebook demonstrates visualization techniques for better understanding of the raw and processed data.

Dependencies

	•	Python 3
	•	Pandas
	•	NumPy
	•	Matplotlib
	•	Seaborn
	•	Scikit-Learn
	•	PyWavelets
	•	ipywidgets

Usage

Data Loading and Preprocessing

The data is loaded from a CSV file, with preprocessing steps to handle missing values and format date entries. The load_and_preprocess_soil_data function reads the data, converts the ‘Date’ column into a datetime object, sets it as the index, and forwards fills missing values.

Visualization

The notebook includes several plotting functions to visualize unedited and edited soil moisture (VWC) and temperature data over time. These plots help in visually inspecting the data for any apparent errors or outliers.

Cleaning Data

Spikes in the data are identified and removed based on predefined thresholds. The function blank_out_spikes is used to set values outside these thresholds to NaN, which are then handled during further processing.

Rolling Median Filter

A rolling median filter is applied to smooth the data, which is less sensitive to outliers than a rolling mean. This is particularly useful for temporal data that may have sporadic spikes.

Normalization

Data normalization is performed using MinMaxScaler to scale the soil moisture and temperature data, which is beneficial for any subsequent analytical methods requiring normalized data.

Wavelet Transform

This section is intended for advanced noise reduction using wavelet transforms. The implementation details are to be added.

Output

The processed data is saved to new CSV files at various stages, ensuring that different versions of the datasets are available for further analysis or audit.

Files

	•	DMP_Arapahoe_Ridge.csv: Raw data file.
	•	Cleaned_Soil_Data.csv: Data after initial cleaning.
	•	Cleaned_Scaled_Soil_Data.csv: Final output with normalized data.

Figures

The notebook generates multiple figures illustrating the soil moisture and temperature data, both before and after data cleaning and normalization. Each figure is clearly labeled to indicate whether the data is edited or unedited.

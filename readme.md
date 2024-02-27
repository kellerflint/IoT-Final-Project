# IoT System for Enhanced Respiratory Monitoring and Sleep Apnea Management
This project is a part of the AAI-530 course, Data Analytics and Internet of Things, in the Applied Artificial Intelligence Masters Program at the University of San Diego (USD).

## Project Objectives
- Perform exploratory data analysis on CPAP machine data to gain insights into flow and tidal volume patterns.
- Develop a deep learning model combining CNN and LSTM to accurately forecast flow and tidal volume metrics with a 1-second predictive horizon.
- Utilize CNN + LSTM for classifying asthma cases by analyzing spectrograms of flow, pressure, and tidal volume data.
- Identify key factors contributing to the model's predictive success to guide future improvements and optimizations.

## Contributors:
- Keller Flint (kflintblanchard@sandiego.edu)
- Ben Hopwood (bhopwood@sandiego.edu)
- Angel Benitez (abenitez@sandiego.edu)

## Main Files
- exploratory_data_analysis.ipynb -> EDA and visualization of input data.
- spectrogram_model.ipynb -> Classification model to predict asthma based on spectrograms. 
- model_flow_all.ipynb -> Flow LSTM + CNN timeseries prediction model trained on all subject data.
- model_flow_by_subject.ipynb -> Flow LSTM + CNN timeseries prediction model trained on individual subjects.
- model_tidal_all.ipynb -> Tidal volume LSTM + CNN timeseries prediction model trained on all subject data.

## Acknowledgments
Data Source: Respiratory dataset from PEEP study with expiratory occlusion: https://physionet.org/content/respiratory-dataset/1.0.0/#files-panel

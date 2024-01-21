'ProcessedDataset'
Folder contains fully processed data from pressure & flow sensor array, dynamic circumference tapes, and EIT.
Files are saved in these folders by subject number ('Subject01' through to 'Subject80') e.g. 'ProcessedData_Subject01.csv' through to 'ProcessedData_Subject80.csv'
These files contain data in columns (A:J): 
	'T' - Time [s],
        'P' - Pressure [cmH2O], 
	'Q' - Flow [L/s], 
	'V' - Tidal Volume [L],
	'CC' - Chest Circumference[mm], 
	'AC' - Abdominal Circumference [mm], 
	'Ind' - Inspiratory Indices,
        'T_GA' - Aeration Data Time Array [s], 
	'GA' - Global Aeration', ...
        'Ind_GA' - Aeration Data Inspiratory Indices,
 
'PQ_rawData'
Folder contains raw data and raw data with units processed from pressure & flow sensor array, and dynamic circumference tapes.
Files are saved in these folders by subject number ('01' through to '80')
Files with relevant units (e.g. 'Subject1.csv') contain data in columns (A:H): 
	'time' - time [s], 
	'GaugeP' - Gauge pressure [cmH2O], 
	'InhaleDeltaP' - Inspiratory differential pressure [cmH2O], 
	'ExhaleDeltaP' - Expiratory differential pressure [cmH2O], 
	'Chest' - Chest circumference [mm], 'Abd' - Abdominal circumference [mm], 
	'Depth_chest' - Chest cross-sectional depth [mm], 
	'Width_chest' - Chest cross-sectional width [mm].
Files with raw ADC counts (e.g. 'Subject1_raw.csv') contain data in columns (A:H): 
	'time' - time [s], 
	'GaugeP_ADC' - Gauge pressure, 
	'InhaleP_ADC' - Inspiratory differential pressure, 
	'ExhaleP_DC' - Expiratory differential pressure, 	
	'Chest_counts' - Chest circumference, 
	'Abd_counts' - Abdominal circumference, 
	'Depth_chest' - Chest cross-sectional depth [mm], 
	'Width_chest' - Chest cross-sectional width [mm].

'EIT_rawData'
Folder contains raw data from EIT.
Files are saved in these folders by subject number ('S01' through to 'S80') e.g. 'S01_01_001_01.bin' through to 'S80_01_001_01.bin'
These files contain data as a matrix of pixel values representing regional aeration for a cross-sectional image (32x32 frame) over time (with 50Hz sampling).

'Code'
Folder contains MATLAB code, used in data collection, processing, and visualization.
	'DataCollection_30MAR23.m' - data collection code for pressure & flow sensor array, and dynamic circumference tapes (generating 'PQ_rawData' .mat files)
	'DataConversion_07AUG23.m' - converts raw data and raw data with units ('PQ_rawData') files from .mat to .csv files
	'DataProcessing_29AUG23.m' - combines and processes pressure & flow sensor array, dynamic circumference tapes, and EIT data to generate 'ProcessedDataset' files
	'read_binData.m' - function to read EIT device files 
	'FigureGenerationCode_29AUG23.m' - generates plots of dataset by subject e.g. 'figure-2.png'

'subject-info.csv'
File contains the relevant self-reported demographic/medical information for the 80 subjects, as well as measured chest width and depth.
	Columns A to E (General Information) respectively contain: Subject Number, Sex [M/F], Height[cm], Weight [kg], and Age [years]. 
	Columns F to H (Asthma History) respectively contain: Asthmatic (Yes/No), Medication name, and Frequency of use of asthma medication (units included in column value).
	Columns I to M (Smoking History) respectively contain: History of Smoking (Yes/No), Current Smoker (Yes/No), How long since quit smoking (units included in column values), Smoking Frequency (units included in column values), and Time/Duration as 		a smoker (units included in column value).
	Columns N to R (Vaping History) respectively contain: History of Vaping (Yes/No), Current Vaper (Yes/No), How long since quit vaping (units included in column values), Vaping Frequency (units included in column values), and Time/Duration as a 		vaper (units included in column value).
	Column S contains the trial cohort classification for the subject.
	Columns T to U (Chest Measurements) respectively contain: Chest Depth [mm], and Chest Width [mm].


'figure-1.png' is an illustration representing the data collection systems and locations during the trial
'figure-2.png' is an example plot of the processed dataset for subject 01


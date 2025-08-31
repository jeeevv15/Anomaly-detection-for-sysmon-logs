# Anomaly-detection-for-sysmon-logs
This project aims to detect anomalies in Windows Sysmon logs using data analysis and machine learning techniques. Sysmon provides detailed event logs about process creations, network connections, and other activities which are valuable for detecting suspicious behaviors on endpoints.
# Anomaly Detection in Sysmon Logs

## Features

- Parse Sysmon logs (CSV format)
- Exploratory Data Analysis (EDA) of event data
- Basic anomaly detection using statistical and machine learning methods
- Visualization of detected anomalies

## Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/yourusername/anomaly-detection-sysmon.git
   cd anomaly-detection-sysmon
   ```

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Add Sysmon log data**  
   Place your exported CSV log files in the `data/` directory.

## Usage

1. **Preprocess logs**  
   ```bash
   python src/preprocess.py --input data/sysmon.csv --output data/processed.csv
   ```

2. **Run EDA notebook**  
   Open `notebooks/eda.ipynb` in Jupyter and follow the steps.

3. **Run anomaly detection**  
   ```bash
   python src/detect.py --input data/processed.csv --output results/anomalies.csv
   ```

## Project Structure

```
anomaly-detection-sysmon/
│
├── data/                # Raw and processed log files
├── notebooks/           # Jupyter notebooks for EDA and prototyping
├── src/
│   ├── preprocess.py    # Data cleaning and parsing
│   ├── detect.py        # Anomaly detection logic
│   └── visualize.py     # Plots and reports
├── requirements.txt
├── README.md
└── main.py
```

## References

- [Sysmon Documentation](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon)
- [EVTXtract](https://github.com/williballenthin/python-evtx)
- [Pandas Documentation](https://pandas.pydata.org/)

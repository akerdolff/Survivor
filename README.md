# Survivor Analysis: The Impact of Advantages

## Data Dictionary

|Table|Column Name| Data Type| Description|
|-----|-----------|----------|------------|


## Data Summary

## Data Source

The data source for this project is https://github.com/doehm/survivoR. The version of the data that I downloaded as anb Excel file was survivoR 2.3.6. 

This data source has an MIT License. https://github.com/doehm/survivoR/blob/master/LICENSE.md

## Setup Instructions

Python 3 is required. This project was created using Python 3.12.8.

1. Open the terminal (Mac/Linux) or Command Prompt/PowerShell (Windows).
2. Navigate to the directory where you want to save the cloned repository: 
```
cd <path_to_desired_folder>
```
3. Clone the repository:
```
git clone https://github.com/akerdolff/Survivor
```
4. Navigate to the Survivor directory
```
cd Survivor
```
5. Give the command to create the virtual environment.
	- Mac/Linux: 
	```
	python3 -m venv <environment_name>
	```
	- Windows:
	```
	python -m venv <environment_name>
	```
	- Replace `<environment_name>` with the name you want to give the virtual environment (e.g., `env`)
6. Activate the virtual environment using the prompt
	- Mac/Linux:
	 ```
	 source <environment_name>/bin/activate
	```
	- Windows Command Prompt:
	```
	<environment_name>\Scripts\activate.bat
	```
	- Windows PowerShell: 
	```
	<environment_name>\Scripts\activate.ps1
	```
	- Replace `<environment_name>` with the name you gave your virtual environment.
7. Once you successfully activate the environment, you should see a prefix of the name of the environment in parenthesis at the start of the line in the terminal
8. Install the dependencies in the virtual environment:
```
pip install -r requirements.txt
```
9. Run the notebook Survivor_Data_Wrangling.ipynb
10. Run the notebook Survivor_Analysis.ipynb
11. To deactivate the virtual environment when you are done: 
```
deactivate
```


## Project Overview

## Technologies used
- Jupyter Notebook: Used to house coding and narrative
- Python: 
- Pandas: Used for cleaning and feature engineering
- SQLite: Used to create a database and perform SQL queries
- Git and GitHub: Used for version control
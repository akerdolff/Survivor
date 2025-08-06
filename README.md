# Survivor Analysis: The Impact of Advantages

## Data Dictionary
**Castaways**

| Field Name            | Data Type | Description                                                                                                                                        | Source        |
| --------------------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| Version               | str       | Several countries have produced their own versions of Survivor. This indicates what country a record is associated with.                           | Original data |
| Version_Season        | str       | Combination of Version and Season.                                                                                                                 | Original data |
| Season                | int64     | Season number. The first season of each version of Survivor is 1 and increments up by 1 each season.                                               | Original data |
| Full_Name             | str       | The full name of the individual competing in Survivor.                                                                                             | Original data |
| Castaway_Id           | str       | A unique ID for each individual who has competed in the show. The same ID is used for each season an individual competed in.                       | Original data |
| Order                 | int64     | The order the an individual exited from the show during a season. 1 is the first person voted out.                                                 | Original data |
| Result                | str       | Indicates vote out order, medical evacuation, runner-up, or sole survivor.                                                                         | Original data |
| Jury_Status           | str       | The order an individual joined the jury. e.g., 1st jury member                                                                                     | Original data |
| Place                 | int64     | The finishing order of a season. 1 signifies an individual is the winner and numbers increase until reaching the first player to leave the season. | Original data |
| Jury                  | bool      | True indicates individual was a member of the jury.                                                                                                | Original data |
| Finalist              | bool      | True indicates the individual was a finalist, but did not win the season.                                                                          | Original data |
| Winner                | bool      | True indicates the individual won the season.                                                                                                      | Original data |
| Season_Castaway_Id    | str       | Primary Key. Unique ID representing an individuals participation in a specific season.                                                             | Engineered    |
| Finale_Categorization | str       | Categorizes each player based on whether their place within the season was pre-jury, jury, finalist, or winner.                                    | Engineered    |
| Era                   | str       | Categorizes each season into an era.                                                                                                               | Engineered    |

**Advantage Details**

| Field Name          | Data Type | Description                                                                                                              | Source        |
| ------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------ | ------------- |
| Version             | str       | Several countries have produced their own versions of Survivor. This indicates what country a record is associated with. | Original data |
| Version_Season      | str       | Combination of Version and Season.                                                                                       | Original data |
| Season              | int64     | Season number. The first season of each version of Survivor is 1 and increments by 1 each season.                        | Original data |
| Advantage_ID        | str       | ID assigned to each advantage within a season. There is duplication between seasons.                                     | Original data |
| Advantage_Type      | str       | The type of advantage, such as Hidden Immunity Idol or Steal a Vote                                                      | Original data |
| Clue_Details        | str       | Indicates where a clue was obtained or whether an advantage was found without a clue                                     | Original data |
| Location_Found      | str       | Indicates where the advantage was found                                                                                  | Original data |
| Conditions          | str       | Indicates any conditions that must be met in order to use the advantage or that affect the power of the advantage        | Original data |
| Season_Advantage_ID | str       | Primary Key. Unique ID representing each advantage within a season.                                                      | Engineered    |


**Advantage Movement**


| Field Name          | Data Type | Description                                                                                                                             | Source        |
| ------------------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| Version             | str       | Several countries have produced their own versions of Survivor. This indicates what country a record is associated with                 | Original data |
| Version_Season      | str       | Combination of Version and Season                                                                                                       | Original data |
| Season              | int64     | Season number. The first season of each version of Survivor is 1 and increments by 1 each season                                        | Original data |
| Castaway_Id         | str       | A unique id for each individual who has participated in the show                                                                        | Original data |
| Advantage_Id        | str       | ID assigned to each advantage within a season. There is duplication between seasons.                                                    | Original data |
| Sequence_Id         | int64     | Provides an order for the Events that occurred with an advantage                                                                        | Original data |
| Event               | str       | Indicates whether a movement was finding/receiving an advantage, playing an advantage, or leaving the show with the advantage           | Original data |
| Success             | str       | For advantages that were played, this indicates whether the advantage was used successfully or not, or if the advantage wasn't needed.  | Original data |
| Season_Advantage_Id | str       | ID that is unique within a season                                                                                                       | Engineered    |
| Season_Castaway_Id  | str       | Unique ID representing an individuals participation in a specific season                                                                | Engineered    |
| Movement_Id         | str       | Primary Key. Unique ID assigned to each advantage movement                                                                              | Engineered    |


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
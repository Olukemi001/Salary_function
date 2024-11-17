# Salary_function
This project includes Python and R scripts for managing employee data. The Python scripts allow users to retrieve employee details from a CSV file, export the data into a ZIP archive, and handle errors gracefully. The R script extracts and displays the contents of the ZIP archive. These tools streamline employee data management and visualization.


## Overview
This project includes Python and R scripts designed to:
1. Process and retrieve employee data from a CSV file.
2. Export selected employee details to a ZIP archive containing a CSV file.
3. Extract and display the contents of the ZIP archive in R.

These scripts are designed for use in environments where employee data is stored in CSV format, allowing users to query and export specific records easily.

---

## Python Scripts

### 1. Employee Data Retrieval
This script allows users to search for employee details by name from a CSV file.

Key Features:
Reads a CSV file into a pandas DataFrame.
Handles case-insensitive name searches.
Retrieves and displays:
  - The most recent salary details.
  - Full details of the employee across multiple years.

Usage:
1. Place the `Total.csv` file in the specified path (`C:/Users/USER/Desktop/Salary_Function_Codes/`).
2. Run the script and enter the employee name when prompted.
3. Outputs:
   - Latest salary details.
   - All historical records of the employee.



 2. Export Employee Data to ZIP
This script exports an employee's details into a CSV file and compresses it into a ZIP archive.

Key Features:
- Allows dynamic specification of the ZIP archive location.
- Automatically removes the CSV file after zipping.
- Handles cases where employee data is not found.

**Usage:**
1. Specify the ZIP archive location or press enter to use the default desktop path.
2. Enter the employee name when prompted.
3. Outputs:
   - A ZIP file (`Employee_Profile.zip`) containing the employee's data in CSV format.

---

## R Script

### **Extract and Display Employee Data**
This script unzips the employee data archive created by the Python script and displays its contents.

**Key Features:**
- Extracts files from the ZIP archive.
- Identifies and reads the first CSV file found.
- Displays the employee data.

**Usage:**
1. Place the ZIP archive in the specified path (`C:/Users/USER/Desktop/Salary_Function_Codes/`).
2. Run the script in R.
3. Outputs:
   - Confirmation of successful extraction.
   - Listing of extracted files.
   - The content of the employee CSV file.

---

## Prerequisites

### Python
- **Libraries**:
  - `pandas`: For CSV file processing.
  - `os`: For file path operations.
  - `zipfile`: For creating ZIP archives.
- **Python Version**: >=3.6.

### R
- **Functions Used**:
  - `unzip`: For extracting ZIP archives.
  - `read.csv`: For reading CSV files.
- **R Version**: >=3.6.

---

## File Paths

### Python
- CSV input file: `C:/Users/USER/Desktop/Salary_Function_Codes/Total.csv`.
- ZIP archive output: Specified by the user or defaults to the desktop.

### R
- ZIP archive input: `C:/Users/USER/Desktop/Salary_Function_Codes/Employee_Profile.zip`.
- Unzip location: `C:/Users/USER/Desktop/Salary_Function_Codes/`.

---

## Error Handling

### Python
- **File Not Found**: Ensures the specified CSV file exists.
- **Empty Data**: Validates that the CSV file is not empty.
- **Missing Columns**: Checks for required columns (`EmployeeName`, `Year`, `TotalPayBenefits`).

### R
- **File Not Found**: Confirms the ZIP archive exists at the specified location.
- **CSV Not Found**: Checks for `.csv` files in the extracted contents.

---

## Example Workflow

1. **Retrieve Employee Data**:
   - Run the Python script to view employee details.
   
2. **Export Data to ZIP**:
   - Use the Python script to create a ZIP archive of the employee's data.

3. **Extract and View Data**:
   - Use the R script to extract and display the contents of the ZIP archive.


## Current Limitations:
- Hardcoded file paths; consider making paths configurable.
- Python script assumes a specific structure for `Total.csv`.



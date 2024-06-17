# Description for Reader
Here is a "mock" code of a security scanning project that I have created during my time at Fairbanks Morse Defense

# Security Project

This project gathers information from depositories and constructs three organized CSV files ranked by severity: "High", "Medium", and "Low". Each CSV file contains data broken down into nine attributes: "Name", "IP Address", "Vuln_Num", "Severity", "Check_Content", "Fix_Text", "Status", "Source", and "Date". The output files are located in the "Output" folder, ordered by the date they were constructed.
------

## Tech/Framework Used

This project is created with:

- Python
- Bash
- Crontab

## Installation

To manually run the code, follow these steps:
1. Open a new Terminal or connect via SSH.
2. Navigate to the project directory: 
```
cd home/Security/firstfolder
```
3. Ensure the script is executable: 
```
chmod +x redactedbash.sh
```
4. Execute the bash script: 
```
./redactedbash.sh
```
5. Enter your password when prompted.
6. Check the "Output" folder for the updated CSV files--the "Output" folder can be found in the "Security" folder.

**Note:** Ensure that all necessary files are placed in the correct directories. You may need to run `chown +x` on the script if file permissions are lost during transfer.

## Usage

The application processes Security checklists, extracts relevant data, and sorts it into CSV files categorized by severity. The attributes included in the CSV files are: "Name", "IP Address", "Vuln_Num", "Severity", "Check_Content", "Fix_Text", "Status", "Source", and "Date".

### Application's functionality:

The application processes security checklists, extracts relevant data, and sorts it into CSV files categorized by severity. The attributes included in the CSV files are: "Name", "IP Address", "Vuln_Num", "Severity", "Check_Content", "Fix_Text", "Status", "Source", and "Date"

### Running the Application:

To run the application, use the following commands:
1. Navigate to the project directory:
   ```
   cd /path/to/bash/script
   ```
2. Execute the main bash script:
   ```
   ./redactedbash.sh
   ```
This command runs the Python script, which processes the data and generates the CSV files in the "Output" folder.

### Scheduling with Crontab:

1. Open the crontab file for editing:
   ```
   sudo crontab -e
   ```
2. Add the following line to schedule the script to run at your preferred time--you must add your edits:
   ```
   * * * * * /path/to/bash/script/redactedbash.sh
   ```
This example will run the script daily at midnight. Adjust the timing as necessary. The format for scheduling is:
- `* * * * *` (minute, hour, day of month, month, day of week)
- For example, `0 0 * * *` means "every day at midnight".

### Finding LOG Information:

To find the Security log information:

1. Open Terminal--if not opened:
2. Add the following command to open the log path and click enter:
```
cd var/log 
```
3. Add the following line to open the log lists--here you may check if the desired log `security.log` exists--and click enter:
``` 
ls -l
```
4. Finally, add the following line to open the log file:
```
cat security.log
```

## Additional Information

### Python Script (redactedpython.py)

The Python script handles the extraction and sorting of data from .ckl files. It creates three CSV files categorized by severity: High, Medium, and Low. The script extracts and organizes data attributes such as "Name", "IP Address", "Vuln_Num", "Severity", "Check_Content", "Fix_Text", "Status", "Source", and "Date"

### Bash Script (redactedbash.sh)

The bash script runs the evaluation process and then executes the Python script. It ensures that the entire process, from data extraction to CSV generation, is automated.

### Directory Structure

```
/security
├── firstfolder/
│   ├── secondfolder/
│   │   └── thirdfolder/
│   │       └── fourthfolder/
│   ├── Output/
│   ├── redactedpython.py
│   └── redactedbash.sh
├── Securityfolder/
│   └── securityinfo/
│       └── Evaluate-security-info.sh
└── README.md
```

## Conclusion

This project simplifies the process of evaluating security checklists and generating organized reports. By following the installation and usage instructions, you can easily run the scripts and obtain up-to-date CSV files with the extracted data. 

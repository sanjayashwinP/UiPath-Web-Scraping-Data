## Exercise_5-UiPath-Web-Scraping
### NAME:SANJAY ASHWIN P 
### REG NO:212223040181
## Aim:
To automate the process of scraping structured data from a website using UiPath and saving the extracted data into a CSV file for further use.

## Equipment Required:
UiPath Studio – Installed and ready to create automation workflows.<br>
Web Browser (Microsoft Edge, Google Chrome, etc.) – A browser to access the webpage from which data will be scraped. Ensure the UiPath Browser Extension is installed.<br>
Internet Connection – For accessing the website.<br>
Computer Specifications:<br>
Minimum 4 GB RAM.<br>
Minimum 2.0 GHz CPU.<br>
Windows operating system.<br>
CSV File Location – Path to save the resulting CSV file after scraping the data.
## Procedure:
### Create a New Process in UiPath Studio:

Launch UiPath Studio and click on Process under the New Project tab.<br>
Name the project (e.g., Scrape Web Data to CSV) and click Create.<br>
This will set up a new workspace for the automation workflow.<br>
### Install Browser Extension (if needed):

If you haven't installed the UiPath browser extension for your preferred browser, UiPath will prompt you to do so.<br>
Follow the instructions to enable the extension, which allows UiPath to interact with the webpage.<br>
### Open a Browser with UiPath:

In the Activities panel on the left, search for Use Browser.
Drag the Use Browser activity into the main window of your workflow.<br>
In the Browser URL property, input the URL of the website that contains the table or structured data you want to scrape. For example:<br>
```
"http://127.0.0.1:5500/ex05/static/table.html"
```
This will open the specified website when the workflow is executed.<br>
### Scrape Data from the Webpage:

Inside the Use Browser activity, drag the Extract Table Data activity.<br>
Use the Data Scraping Wizard to scrape the structured data from the webpage:<br>
Click Extract Table Data and a wizard will appear.<br>
Select the first and second elements of the table or data list you want to scrape.<br>
The wizard will automatically highlight similar elements on the page and capture them.<br>
Once the pattern is recognized, you can customize the data by renaming the columns or refining the selection.<br>
The extracted data is automatically stored in a DataTable variable (for example, ExtractDataTable).<br>
### Save Scraped Data to CSV File:

After the Extract Table Data activity, search for Write CSV in the Activities panel and drag it into the workflow.<br>
Set the Write from field to ExtractDataTable, the variable holding the scraped data.<br>
In the Write to what file property, specify the file path where you want the CSV to be saved. For example:<br>
```
"C:\Users\admin\Documents\UiPath sample csv.csv"
```
Ensure the Include headers checkbox is checked so that column names from the table will be added to the CSV file.<br>
### Configure and Test:

Verify that all paths are correct and all activities are connected.<br>
Save the project by pressing CTRL+S.
### Run the Automation:

Click the Run button at the top of UiPath Studio.<br>
The workflow will:<br>
Open the specified website in the browser.<br>
Extract the data from the table or structured list on the webpage.<br>
Write the extracted data into the CSV file at the specified location on your system.<br>
### Check the CSV Output:

Navigate to the location of your saved CSV file.<br>
Open the CSV file to verify that the scraped data has been written correctly, including the headers if applicable.<br>
### Example Scenario:
Web Page: A website displays a table of customer information (e.g., names, addresses, phone numbers, etc.).
### UiPath Workflow Actions:
Open the browser and navigate to the web page.<br>
Scrape the table data (e.g., the names and phone numbers) using the Data Scraping Wizard.<br>
Save the scraped data in a CSV file named CustomerData.csv in the Documents folder.<br>
### Output:
The CSV file contains two columns: "Name" and "Phone Number".<br>
Each row represents the customer information extracted from the table on the webpage.
## UiPath WorkFlow:
![alt text](<img/Screenshot 2024-09-17 114233.png>)
![alt text](<img/Screenshot 2024-09-17 114534.png>)
![alt text](<img/Screenshot 2024-09-17 114555.png>)
![alt text](<img/Screenshot 2024-09-17 114630.png>)
![alt text](<img/Screenshot 2024-09-17 115204.png>)
## Result:
The workflow successfully scrapes data from the target webpage, saves the data in a structured format in a CSV file, and includes headers for the data columns. This shows that UiPath can easily automate data extraction tasks and save the data for future processing, analysis, or reporting.

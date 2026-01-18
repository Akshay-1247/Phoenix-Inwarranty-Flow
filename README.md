# Postman API Automation Integration with Github Actions #

This repository demonstrates a Proof of Concept (POC) for integrating Postman API tests with GitHub Actions.
The tests are written in postman and are executed on the virtual machine with the help of newman.  
The GitHub Actions workflow is triggered:  
- On every push to the ```main``` branch
- Manually via workflow_dispatch
- On a scheduled basis using a cron job

The HTML reports are archived and kept in the artifacts section for the team to download.  
Along with that they can view the report directly from the github pages: https://akshay-1247.github.io/Phoenix-Inwarranty-Flow/  
The latest report is mailed to the team using GMAIL SMTP.

## About Me ##
Hi, I’m Akshay Halurkar, an Automation Tester with 4.5 years of experience.  
My skillsets include  
- API Automation
- Mobile UI Automation
- CI/CD integrations for test automation

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing
3. Token Testing
4. Data Driven Testing with csv
5. Schema Validations
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Nodejs v22
3. Newman
4. Newman-reporter-htmlextra
5. GitHub Actions
6. Gmail SMTP
7. Github Pages
8. CSV (Data-Driven TEsting)

## Github Pages ##
You can directly view the test report of the postman tests at the Github Page link: https://akshay-1247.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The report will be created in the Newman Folder
![Newman Report](https://github.com/Akshay-1247/Phoenix-Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##
```
PhoenixInWarrantyFlow
├─ DataDrivenInwarranty.json # Collection File
├─ QA.postman_environment.json # Environment File
└─ testData2.csv # Testdata file
```

## How to run the project ##
You can run the project on your local system
1. Clone the Project on local system: https://github.com/Akshay-1247/Phoenix-Inwarranty-Flow.git
2. Install nodejs and npm
3. Install Newman using: ```npm install -g newman```
4. Install newman-reporter-htmlextra: ```npm install -g newman-reporter-htmlextra```
5. Run the newman command:
 ```
	newman run DataDrivenInwarranty.json \
             -e QA.postman_environment.json \
             -d testData2.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
   ```

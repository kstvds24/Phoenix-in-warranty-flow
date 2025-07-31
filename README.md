# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for Integrating postman tests with github actions. The tests are written in postman and executed on the VM with the help of newman and newman-reporter-htmlextra.
Github actions will trigger the project execution on every push to the main branch. In order to run the project manually we have also used workflow_dispatch. The Project runs on scheduled time with the help of cron jobs.

The html report is archieved and kept in the artifact section for the team to download it. Along with that they can view from github page: https://kstvds24.github.io/Phoenix-in-warranty-flow/.
The latest report is also mailed to the team members using GMAIL SMTP

## About Me ##
Hi my name is Kaustav Das, I have 10+ years of experience in automation testing and Devops. My skillset incudes UI automation with Selenium Webdriver, Cypress, Playwright and for API testing I use Rest Assured and Postman.
You connect with me over: https://www.linkedin.com/in/kaustav-das-200710116/

## Testing Coverage ##
1. Happy FLow testing
2. Negative and Edge case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with GitHub Secrets

## Tech Stats ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Git Hub Actions
6. Gmail SMTP
7. GitHub Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self hosted git hub runner

## GitHub Pages ##
You can directly view the latest report of the postman tests at the GitHub Page Link: https://kstvds24.github.io/Phoenix-in-warranty-flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/kstvds24/Phoenix-in-warranty-flow/blob/static-content/Neman-Report.png)

## Project Structure ##
```
Phoenix in warranty
├─ Inwarranty-flow Collection.postman_collection.json # Collection File
├─ QA.postman_environment.json # Environment File
└─ testdata.csv # TestData File

```

## How to Run the Project? ##
You can run the project on your local machine, for that
1. Clone the Project on your Local System: ``` https://github.com/kstvds24/Phoenix-in-warranty-flow.git ```
2. Install Nodejs: ``` https://nodejs.org/en/download ```
3. Install Nemann using ``` npm install -g newman ```
4. Install Newman-reporter-htmlextra using ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman command:
   ```
              newman run 'Inwarranty-flow Collection.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
  ```

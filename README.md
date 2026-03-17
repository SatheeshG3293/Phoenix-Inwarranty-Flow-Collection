# Postman API Automation Integration with GitHub Actions

This repository is a proof of concept (POC) for integrating Postman tests with GitHub Actions. The tests are written in Postman and executed on a VM using Newman and newman-reporter-htmlextra.

GitHub Actions triggers the project execution on every push to the `main` branch. You can also execute the project manually using `workflow_dispatch`, or schedule it using a cron trigger.

The HTML report is archived as a workflow artifact for download, and can also be viewed via GitHub Pages:
https://satheeshg3293.github.io/Phoenix-Inwarranty-Flow-Collection/

Latest reports are emailed to the team using Gmail SMTP.

## Testing Coverage
1. Happy flow testing
2. Negative testing and edge case testing
3. Token testing
4. Data-driven testing with CSV
5. Schema validation
6. Secrets management using GitHub Actions

## Tech Stack
1. Postman
2. Node.js 22
3. npm
4. Newman
5. newman-reporter-htmlextra
6. GitHub Actions
7. Gmail SMTP
8. GitHub Pages
9. CSV for data-driven testing
10. AWS EC2 (self-hosted GitHub runner)

## GitHub Pages
You can directly view the latest test report on GitHub Pages:
https://satheeshg3293.github.io/Phoenix-Inwarranty-Flow-Collection/

## HTML Report
The following report is generated under the `newman/` folder:

![Postman Report](https://raw.githubusercontent.com/SatheeshG3293/Phoenix-Inwarranty-Flow-Collection/Static-content/Newman%20Report%20Format.png)

## Project Structure

```
Phoenix Inwarranty Flow Collection
├─ Inwarrenty Flow Collection.postman_collection.json # Collection file
├─ QA.postman_environment.json # Environment file
├─ testdata.csv # Test data file
└─ Testfile.txt
```

## How to Run the Project
1. Clone the project:
   ```sh
   git clone https://github.com/SatheeshG3293/Phoenix-Inwarranty-Flow-Collection.git
   ```
2. Install Node.js and npm: https://nodejs.org/en/download
3. Install Newman:
   ```sh
   npm install -g newman
   ```
4. Install the HTML reporter:
   ```sh
   npm install -g newman-reporter-htmlextra
   ```
5. Run the collection:
   ```sh
   newman run 'Inwarrenty Flow Collection.postman_collection.json' \
     -e QA.postman_environment.json \
     -r htmlextra,cli \
     --reporter-htmlextra-export ./newman/index.html
   ```

## About Me
Hi, my name is Satheesh Kumar Ganesh. I have 9+ years of experience in both manual and automation testing.

My skillset includes UI automation with Selenium WebDriver and Tricentis Tosca, and API testing using Postman, Rest Assured, and Parasoft SOATest.

You can connect with me: https://www.linkedin.com/in/satheesh-kumar-ganesh-70897099/


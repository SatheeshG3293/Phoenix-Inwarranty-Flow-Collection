# Postman API Automation Integration with Github Actions #

This Repository is a demonstration for POC for integrating postman tests with github actions. The Tests are written in Postman and they are executed on the VM with the help of newmand and newman-reporter-htmlextra.
GitHub Actions will trigger the project execution on every push to the main branch. you can also execute the project manually using workflow_dispatch and the project run on a scheduled time with the help of Cron.

The HTML is archeived and kept in artifact section for the team to download it. Along with that they can view the report from the github page: https://satheeshg3293.github.io/Phoenix-Inwarranty-Flow-Collection/ 

The Latest Report mailed to the Team members using the GMAIL SMTP.

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Scheman Validation
6. Secrets management using Github Actions

## Tech Stack ##
1. Postman
2. Node js 22v
3. npm
4. Newman
5. Newman-reporter-htmlextra
6. Github Actions
7. GMAIL SMTP
8. Github Pages
9. CSV for Data Driven Testing
10. AWS-EC2 instance for Self Hosted github runner.

## Github Pages ##

you can directly view the latest test reoprt of the Postman Test at Github Page URL: https://satheeshg3293.github.io/Phoenix-Inwarranty-Flow-Collection/

## HTML Report ##
The Following Report will be Created in the Newman Folder

![Postman Report](https://raw.githubusercontent.com/SatheeshG3293/Phoenix-Inwarranty-Flow-Collection/Static-content/Newman%20Report%20Format.png)


## Project Structure ##

```
Phoenix Inwarranty Flow Collection
├─ Inwarrenty Flow Collection.postman_collection.json #Collection File
├─ QA.postman_environment.json #Environment file
├─ testdata.csv #Test data file
└─ Testfile.txt

```

## How to Run the Project ##
You can run the project in the local systems for that:

1. Clone the Project on the Local System: https://github.com/SatheeshG3293/Phoenix-Inwarranty-Flow-Collection.git
2. Install the node.js and NPM from : https://nodejs.org/en/download
3. Install newman using ```npm install -g newman```
4. Install newman-html using ```npm install -g newman-reporter-htmlextra```
5. Run the newman command:
 ```
           newman run 'Inwarrenty Flow Collection.postman_collection.json' \
          -e QA.postman_environment.json \
          -r htmlextra,cli \
          --reporter-htmlextra-export ./newman/index.html
```

## About me ##

Hi My name is Satheesh Kumar Ganesh. I have 9+ Years of Experience in both Manual and automation Testing.
My skillset includes UI Automation with Selenium Webdriver and Tricentis Tosca and API Testing I use Postman, Rest Assured and Parasoft SOATest.

you can connect with me: !(https://www.linkedin.com/in/satheesh-kumar-ganesh-70897099/)

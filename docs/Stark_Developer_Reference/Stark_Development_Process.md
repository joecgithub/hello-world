# Stark Development Process
Stark follows an internal open-source model. All developers within Millennium are welcome to contribute and re-use code. Stark developers follow the process described here.

## 1. Checkout the code

-   Check out the code base [here](http://luxgit.mlp.com/algo-execsvcs/stark).
-   If you don't have access, email [StarkDev](mailto:StarkDev@mlp.com) to request it.

  

## 2. Create a JIRA

-   Go to the [JIRA projects page](https://jira.mlp.com/projects/AX/summary).
-   Document your change. If soliciting input, you can use JIRA comments, and the @ sign to ask specific people questions to. Comments keep the conversation history, open to the public. We try to avoid using emails.

  

## 3. Create a Feature Branch

-   Create a feature branch using the following convention:  
    
          feature/AX-999  (where AX-999 is your JIRA number)
    

  

## 4. Commit Your Code

-   Start with the JIRA number.
-   Write a meaningful comment describing your change.
-   Once you commit your code, the JIRA will be automatically transitioned to "In Progress."

  

## 5. Run Unit Tests

-   Your branch must pass all unit tests before it can be merged.
-   If you think unit test failures are unrelated to your change, email [StarkDev](mailto:StarkDev@mlp.com).

  

## 6. Create a Pull Request

-   Create a pull request to [the master branch](http://luxgit.mlp.com/algo-execsvcs/stark/pulls](http://luxgit.mlp.com/algo-execsvcs/stark/pulls).
-   GitHub will re-run all unit tests and only if they pass will it allow the request to be merged.
-   Check your pull request for comments and questions, and respond directly on the pull request (again, we try to avoid emails).
-   The JIRA will automatically transition to "In Review"

## 7. Pull Requests Management Guidelines

To keep the number of open pull requests manageable, we follow these guidelines:

- Keep pull requests small. It's better to send smaller, incremental pull requests rather than large ones with dozens of file changes. If the code is not complete, stub out not yet implemented parts. The code can be merged so long as it does not break existing functionality.
- Avoid long-living pull requests: they should be actively worked on and/or reviewed. If a pull request persists more than a week without being worked on, close it then reopen later.
- Pull request labels have the following meaning:

| Label | Meaning |
|--------|--------|
|No Label        |Pull request has just been created and is ready for merging pending approval by at least one other developer.|
|**changes requested**        |Another developer has reviewed the pull request and asked for changes to be done.|
|**requested changes done** |Original developer has addressed all the requested changes and the code is ready to be reviewed again.|
|**approved** | At least one other developer has approved the pull request and it can be merged.|
|**request for comment** | For soliciting early feedback only. Code is not yet complete and is not intended to be merged as is.
## 8. When Your Pull Request Is Accepted

-   It will get merged to master and your changes will be available in the [new Jenkins build](http://rfpluxd01:8080/jenkins/view/STARK/job/stark/),
-   and in [artifactory](http://rfpluxd01:8082/artifactory/webapp/home.html?0).
-   The JIRA will automatically transition to "QA".  
      
    

## 9. The next morning. . .

- Integration tests run nightly [here](http://rfpluxd01:8080/jenkins/view/STARK/job/stark-soms-integration-tests/).
- If your change caused an integration break, you will receive an email from StarkDev. If it can't be fixed the same, day it might be reverted:

 ### **Otherwise, Congratulations -- Your change is in!**

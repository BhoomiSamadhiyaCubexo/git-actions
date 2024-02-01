**Github actions**
    - Github actions is a continuous integration and continuous delivery(CI/CD) platform that allows to build, test and deployment pipeline. 
    - We can create workflows that build and test every pull request to your repository, or deploy merged pull requests to production. 

**Componenets of Github actions**
    - Github Actions Workflow is triggered by an event occuring in the repository.
    - One or more jobs can run in sequential or in parallel order in a workflow. 
    - Each _job runs in it's own virtual machine runner_, **or** _inside a container_, and **has one or more steps** that _either run a script that you define_ **or** _run an action, which is a reusable extension that can simplify your workflow._

EVENT ---> RUNNER1 ---> RUNNER2
             |             |
            JOB1         JOB2

**Workflows**
    - Configurable process
    - automated process
    - that runs one or more jobs
    
    - workflows are YAML file 
    - runs when 
        - triggered by an event in your repository
        - can be managed manually 
        - can be scheduled
    - defined in the .github/workflows directory in a repository
    - a repo can have more than one workflows 
        - each of the workflows can perform a different set of tasks.

**Events**
    - An event is a specific activity in a repository
    - It triggers the workflow run
    - Trigger a workflow
        - to run a schedule, by posting to a REST API
        - or, manually
    
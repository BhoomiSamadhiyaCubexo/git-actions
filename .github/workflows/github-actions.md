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
    
**Jobs**
     - set of steps in a workflow executed on the same runner 
     - each step is 
          - either shell script taht will be executed
          - or an action that will be run 
     - each step is independent of another and run independently
     - data sharing is possile as all steps run on same runner 
     - job's dependencies can be configured with other jobs 
          - by default, jobs have no dependencies and run in parallel with each other
          - When a job takes a dependency on another job, it will wait for the dependent job to complete before it can run.
    
**Actions**
     - a custom application for github actions platform 
     - it performs a complex but frequently repeated task
     - used to reduce the amount of repetitive code that we write in workflow files.
     - An action can pull your git repository from GitHub, set up the correct toolchain for your build environment, or set up the authentication to your cloud provider.
     - You can write your own actions, or you can find actions to use in your workflows in the GitHub Marketplace.

**Runners**
     - it is a server that runs your workflows when they're triggered
     - each runner can run a single job at a time 
     - GitHub provides Ubuntu Linux, Microsoft Windows, and macOS runners to run workflows
     - each workflow run executes
          - in a newly provisioned,
          - fresh VM
    
          
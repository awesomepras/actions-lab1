# GitHub Actions Labs
files related to github actions tutorials

# what is it:
To automate tasks, a workflow is needed.  
A workflow consists of jobs.  
A job contain list of steps, which GitHub executes in sequence. 

![source microsoft](https://learn.microsoft.com/en-us/training/github/github-actions-automate-tasks/media/github-actions-workflow-components.png)

A step can be commands or an action (pre-built or reusable) 
# how does it do it:
 GitHub looks for YAML files inside of the .github/workflows directory.


```
<name>:
<trigger event>(typically on pull_req or push)
jobs:
  <name>:
  runs-on: <something -typically a runner>
  steps: 
  - name:
    <dosomething>
  -uses: actions/checkout@v2 # reusable/pre-built
```

# Configuration of GHAWF: 
A workflow can be triggered via
* schedule event (cron)  
* Manual event  
    * workflow_dispatch event  
    * repository_dispatch event  
* A webhook event (to run a WF)  

## workflow_dispatch
Allows running workflow using button in the Actions tab within your repository on GitHub.or use Github REST API. 
## repository_dispatch 
Allows triggering a webhook for an activity outside of Github. 

# Workflow as a template 
Any workflow can be promoted to organization's .github repository as a workflow template that can be used by multiple teams.  

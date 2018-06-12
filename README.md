# concourse-branch-manager learning material
  -  https://github.com/pivotaltracker/concourse-branch-manager

# pre-requiste steps for this repo code execution
  - update your github private key in `secrets.yml` file
  - update your github repository path in `pipeline.yml` file
      - line 11, 26
  - provision a pipeline server    

# execution commands (for login & set pipeline)
  - fly -t targetName login --team-name main --concourse-url yourServerUrl
  - fly -t targetName sp -p pipelineName -c ci/pipeline.yml -l ci/secrets.yml 

# git branch creation
```
$ git checkout -b feature/dddd
Switched to a new branch 'feature/dddd'

$ git push origin feature/dddd
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/xxx/concourse-branch.git
 * [new branch]      feature/dddd -> feature/dddd
```

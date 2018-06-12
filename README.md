# concourse-branch-manager
  -  basic set up

# pre-requiste
  - update your github private key in `secrets.yml` file
  - update your github repository path in `pipeline.yml` file
      - line 11, 26
  - provision a pipeline server    

# execution commands (for login & set pipeline)
  - fly -t target1 login --team-name main --concourse-url yourServerUrl
  - fly -t target1 sp -p home1branch1 -c ci/pipeline.yml -l ci/secrets.yml 

# git branch creation
```
$ git checkout -b feature/dddd
Switched to a new branch 'feature/dddd'

$ git push origin feature/dddd
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/xxx/concourse-branch.git
 * [new branch]      feature/dddd -> feature/dddd
```

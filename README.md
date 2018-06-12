# concourse-branch-manager
  -  basic set up

# pre-requiste
  - update your github private key in `secrets.yml` file
  - update your github repository path in `pipeline.yml` file
      - line 11, 26
  - provision a pipeline server    

# execution commands (for login & set pipeline)
  - fly -t target1 login --team-name main --concourse-url <serverUrl>
  - fly -t target1 sp -p home1branch1 -c ci/pipeline.yml -l ci/secrets.yml 

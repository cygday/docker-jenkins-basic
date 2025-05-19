jenkins setup notes
- jenkins must run on a node with docker installed.
- the jenkins user must have  permission to run Docker (usually by being in
    the docker group).
- you may need to enable docker pipeline plugin in jenkins


this job will:
- clone the repo
- build a docker image from the dockerfile
- run the container and output logs



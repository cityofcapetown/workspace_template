# workspace_template

## If you have forked this repo, you should replace this README.md file with the README-Template.md file.
### Then populate your new README with useful information about the project.

A template file structure for an OPM hosted data science development environment, intended to be used along with the docker data science image available at `riazarbi/jupyter_from_repo`. 

## Rationale for this repository's existence

The primary reason for its existence is to impose a folder structure and supply the requisite .gitignore files to your environment to promote predictable, well-formed coding behaviour. Good coding practices include -

* Regular committing of code to a code versioning system.
* Embedding data pulls from source in the code rather than referring to local, unauditalbe data.
* Regular offsite backups.
* Avoidance of committing sensitive information or large files to git.

## How this repository behaves

1. Anything you put in the `tempdata` folder will not be committed or pushed to your remote git repo. So put data that you don't want to share in this folder. Ideally the contents of this folder should be pushed to a backup so that you can replicate your project easily by re-cloning your git repo and repopulating the data folder.
2. Anything you put in the `secrets` folder will not be committed or pushed to your remote git repo. Use this folder to store secrets (like usernames, passwords, configs etc). As with the tempdata folder, back this up somewhere private.
3. Anything you put in the root folder (ie the folder that this `README` file resides in) or any other folder you create will be pushed to the remote git repository. So if you commit and push this regularly you are backing up your code. If your remote repository is public, everyone will be able to see these files.
4. The .gitignore file is set to ignore and R and python working files (like .Rdata or .Rproj files).

## Intended use case
### While developing code
1. Fork this repository and rename to something useful, like `MINST_random_forest`.
2. Download the docker image from the above repository.
3. Start a container with the flag `-e GITREPO=<repo url>`. The container will clone the repo into the working directory.
4. Access the jupyter notebook at the URL provided by the container console (see https://jupyter-docker-stacks.readthedocs.io/en/latest/using/running.html#using-the-docker-cli).
5. Include your data acquisition steps programatically (that is, don't upload csvs, `wget` csvs etc so that the data can be retreived programatically).
6. Commit and push your code regularly to avoid disappointment.

When you are done developing, push your code and shut down the container.

### Deploying code
When you are ready to deploy your project, simply download the docker image to your production machine and start a container with the same `GITREPO` flag. Your new container will spin up in the production environment ready to go.

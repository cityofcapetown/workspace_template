# Project Name
> Short blurb about what your product does. For instance:

This codebase contains a jupyter notebook that will read all your emails and compile a PDF report that contains alalytics about the following:

* Your most frequently contacted contacts
* A subject line word cloud
* A count of how many words you have emailed in the last 3 months
* A chart showing the most contacted organizations in your email history

## Changes to base image
> Mention the base image that your started with.

This codebase was developed from the riazarbi/jupyter_from_repo docker image, which was accessed on the 23rd July 2018.

> List any packages added to the environment while developing the project so that somebody can replicate the environment from the same source docker image. 

I added the following python packages:
* pandas
* keyring
* unicodecode

## Deployment instructions
> List anything you have to do to a newly cloned repository to get it running. For instance:

1. Clone this repository to your environment
2. Launch a jupyter notebook
3. Create a file called `credentials` in your `secrets` folder with the following contents:
```
email_address:<youremail@example.com>
password:<your_email_password>
```
4. Open `project_code.ipynb`
5. Run the cells from top to bottom
6. The code will output a PDF report under the root directory. You can download it and distribute it.

## Owner Details

Your Name – YourEmail@example.com
your Role - Your Department - Your Organization

> Any usage/collaboration instructions for people who browse this codebase. For instance, 

I never got very far with this project. If you want to continue development get hold of me and I'll transfer repo ownership to you.

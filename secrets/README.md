# Secrets Folder

This is where you store secrets that you don't want to be push to your git repository.

Anything in this folder will **not** be backed up to the git repository.

You should therefore expect that everything in this folder can be destroyed with no warning. Your code should contain everything required to pull your secrets from an **external** source and store it here temporarily.

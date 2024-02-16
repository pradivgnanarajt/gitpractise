# gitpractise

This is how we authenticate:
Windows:

Using wincred:
git config --global credential.helper wincred
git config --global credential.username <your_username>
git config --global credential.store "password=PAT:<your_PAT>"
macOS/Linux:

Using cache:
git config --global credential.helper cache
git config --global credential.username <your_username>
echo "https://<username>:<your_PAT>@github.com" > ~/.netrc
Using store:
git config --global credential.helper store
git config --global credential.username <your_username>
echo "https://<username>:<your_PAT>@github.com" > ~/.git-credentials

Once the above is done, we verify by :
git config credential.helper

And then we clone the repo to local. Instead of password we use PAT created
under the settings. For now, it is valid for 30 days. 

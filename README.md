# Development guideline
New changes must be initially done in "development" branch. If you wish to merge your code into the master branch do so with caution or with a pull request.

*Read the SSH setup guide before you start contributing*

To start contributing:
```
git clone git@github.com:data-break/<repository-name>.git
cd <repository-name>
git checkout development
```

# Setup SSH for github
You need to setup an ssh key in order to ssh into projects and push with your credentials, follow this guide: [Setting Up SSH Keys for GitHub](https://www.youtube.com/watch?v=8X4u9sca3Io)
As follows:
```
ssh-keygen -t ed25519 -C example@example.com
eval "$(ssh-agent -s)"
touch ~/.ssh/config
```

Edit the config file with your desired text editor:
```
nano ~/.ssh/config
```
Add the following:
```
Host *
	AddKeysToAgent yes
	IdentityFile ~/.ssh/ed_25519
```

Add the SSH key to the agent:
```
ssh-add ~/.ssh/id_ed25519
```

Retrieve the SSH key's public part: ``` cat ~/.ssh/id_ed25519.pub``` and add the output as your github ssh key

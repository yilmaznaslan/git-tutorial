# Git Tutorial

## How git works
## Git Configuration

`git config --global user.name "yilmaznaci.aslan"`
`git config --global user.email "yilmaznaci.aslan@maibornwolff.de`

`git config --global color.ui auto`

`git config`

`git rm -r --cashed .`

`git log`

`git show`

`git diff`

## SSH Key
Main purpose here to generate *private* and *public* key and then push the private key to the Github/Gitlab.

### How to generate SSH Key
`ssh-keygen -t ed25519 -C "yilmazn.aslan@gmail.com`
Click enterx3

### Add the ssh key to ssh-agent
First create .ssh/config file and then paste the following
#### Start the SSh key agent
`eval "$(ssh-agent -s)"`

#### Update thte .ssh/config file
`Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
`
#### Add SSH private key to the ssh-agent
`ssh-add -K ~/.ssh/id_ed25519`


##

`git branch`

`git branch -r`

### See all branch
`git branch -a`

### Create branch
`git branch feature-a`

### Change branch
`git checkout feature-a `

#### Checkout to previous branch
`git checkout -`

### Create branch and checkout to it
`git branch -b feature-x`

### Delete a branch
`git branch -d feature-a`

## Main Workflow
- Pull the latest changes from the master branch of the remote repository into local
- Create a new branch and work on that branch
- Before pushing to remote 
    - squach all of your local commits first 
    - rebase master
    - Solve the conflicts
- Once you are done commit&push the feature to the remote 
- Create pull request and assign reviewers to it.
- Admin will merge it
- Restart a new feature with git pull ...
- Delete the local feature branch that you have pushed.


## Merge Issues

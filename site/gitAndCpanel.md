
# How to clone a private Github repo into Cpanel

## Generate a key in Cpanel

1. Cpanel --> Sequrity --> SSH Access --> Manage Keys --> Generate New Key (enter a strong pasword) 

## Copy the key
1. After generating a key go to SSH Access --> Manage SSH Keys --> Public keys -->  Authorize (make authoize) --> Go back --> Press view/download --> Dowload key.

## Copy public key to Github
2. Go Github --> Your private repo --> Settings --> Deploy Keys --> add deploy key (give title,and add public key).

## Clone a repo to CPanel

1. Make sure you've added a `.cpanel.yml` file at the root of your project that you are uploading. The contents of this file can be something like

```properties
---
deployment:
  tasks:
    - export DEPLOYPATH=/home/ReplaceItByYourUserName/public_html/
    - /bin/rm -Rf $DEPLOYPATH
    - /bin/mkdir $DEPLOYPATH
    - /bin/cp -R FileWhereSiteContentIsLocated/* $DEPLOYPATH
```

 After you upload your project, this file will be hidden (as this is a . file) but can be seen by going to your directory from cPanel home --> Advanced --> Shell

```sh
cd yourHome/Repositories
ls -a
```

1. Go to Cpanel --> Git™ Version Control --> create clone url and enter the similar `Clone URL`

```sh
 git@github.com:<user_name>/<repository_name>.git
```

The `Repository Path` and `Repo Name` will be autofilled. Then hit create.

## Pull from the sources.

1. Manage repository from list --> Manage--> pull or deploy from Github --> Click on Update from Remote: works perfectly (any files edit or delete you fetch/pull from GitHub now)


# How to clone a private Github repo into Cpanel

## Generate a key in Cpanel

1. Cpanel --> Sequrity --> SSH Access --> Manage Keys --> Generate New Key (enter a strong pasword) 

## Copy the key
1. After generating a key go to SSH Access --> Manage SSH Keys --> Public keys -->  Authorize (make authoize) --> Go back --> Press view/download --> Dowload key.

## Copy public key to Github
2. Go Github --> Your private repo --> Settings --> Deploy Keys --> add deploy key (give title,and add public key).

## Clone a repo to CPanel

3. Go to Cpanel --> Git™ Version Control --> create clone url and enter the similar `Clone URL`

```sh
 git@github.com:<user_name>/<repository_name>.git
```

The `Repository Path` and `Repo Name` will be autofilled. Then hit create.

4. Manage repository from list --> Manage--> pull or deploy from Github --> Click on Update from Remote: works perfectly (any files edit or delete you fetch/pull from GitHub now)


 git@github.com:amarjitdhillon/asdhillon.git

Your identification has been saved in /home/amarylyq/.ssh/id_rsa_asdhillon.
Your public key has been saved in /home/amarylyq/.ssh/id_rsa_asdhillon.pub. -->


git clonea


vim ~/.ssh/config

Host cpanelaccountname
        Hostname cpanelaccountname.web.illinois.edu
        IdentityFile ~/.ssh/sshprivatekeyname
        IdentitiesOnly yes



Host amarylyq
        Hostname amarylyq
        IdentityFile ~/.ssh/id_rsa_asdhillon
        IdentitiesOnly yes




        amarylyq


        git clone cpanelaccount@cpanelaccountname:/home/cpanelaccountname/path/to/repo

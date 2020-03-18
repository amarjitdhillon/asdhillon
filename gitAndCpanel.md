
# How to clone a private Github repo into Cpanel

## Generate a key in Cpanel

1. Cpanel --> Sequrity --> SSH Access --> Manage Keys --> Generate New Key (enter a strong pasword) 

<!-- ## Copy the key
1. After generating a key go to under public key --> Manage--> Authorize (make authoize) --> back, now view/download --> Copy key

2. Go Github--> https://github.com// --> Settings -->Deploy Keys (rights side)--> add deploy key (give title,and add key) --> done

3. Go to Cpanel --> Git™ Version Control --> clone url : git@github.com:/.git

```sh
 git@github.com:<user_name>/<repository_name>.git
```
--> give_repository_path

--> give_ repository_name

--> create

4. manage repository from list-> Manage -> pull or deploy from Github -> Click on Update from Remote: works perfectly(any files edit or delete you fetch/pull from GitHub now)


Your identification has been saved in /home/amarylyq/.ssh/id_rsa_asdhillon.
Your public key has been saved in /home/amarylyq/.ssh/id_rsa_asdhillon.pub. -->
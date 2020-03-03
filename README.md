# Demo2
This Is the Repository For Learning SSH Key Use.

# The SSH Protocol
A common transport protocol for Git when self-hosting is over SSH. This is because SSH access to servers is already set up in most places — and if it isn’t, it’s easy to do. SSH is also an authenticated network protocol and, because it’s ubiquitous, it’s generally easy to set up and use.


# Pros
The pros of using SSH are many. First, SSH is relatively easy to set up — SSH daemons are commonplace, many network admins have experience with them, and many OS distributions are set up with them or have tools to manage them. Next, access over SSH is secure — all data transfer is encrypted and authenticated. Last, like the HTTPS, Git and Local protocols, SSH is efficient, making the data as compact as possible before transferring it.

# Cons
The negative aspect of SSH is that it doesn’t support anonymous access to your Git repository. If you’re using SSH, people must have SSH access to your machine, even in a read-only capacity, which doesn’t make SSH conducive to open source projects for which people might simply want to clone your repository to examine it. If you’re using it only within your corporate network, SSH may be the only protocol you need to deal with. If you want to allow anonymous read-only access to your projects and also want to use SSH, you’ll have to set up SSH for you to push over but something else for others to fetch from.



## Adding SSH Key On Linux O.S.

### PART - 1 : On Your Local system

``` 
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]
Enter passphrase (empty for no passphrase): [Type a passphrase]> Enter same passphrase again: [Type passphrase again]
```

Adding SSH Key To SSH Agent

``` 
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

### PART - 2 : On Your GitHub Account

```
Copy the id_rsa_pub file content on clip board.
In Your Github Account > settings >select SSH and GPG option.
Click on "ADD New SSH KEY"
In Title Section Give Appropriate title ex: Personal Laptop , Office PC etc For Unique Identification of each Key
Paste The content in "Key" and click on Add. 

```

# DONE !!! - You have sucessfully added the ssh key.

Use this key for cloning or pushing the repositiory contents.

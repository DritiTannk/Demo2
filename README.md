# Demo2
This Is the Repository For Learning SSH Key Use

Commands For adding Keys are as Follows:

## Linux

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

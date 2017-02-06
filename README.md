# sshkey

## Generate a sshkey

type

    ssh-keygen

in rsp pi terminal, then hit enter til you finish.

example:

    beichen@M2800:~/.ssh$ ssh-keygen
    Generating public/private rsa key pair.
    Enter file in which to save the key (/home/beichen/.ssh/id_rsa): 
    Enter passphrase (empty for no passphrase):  
    Enter same passphrase again: 
    Your identification has been saved in /home/beichen/.ssh/id_rsa.
    Your public key has been saved in /home/beichen/.ssh/id_rsa.pub.
    The key fingerprint is:
    SHA256:B6GUQCyzS3zyh9tT+JPPF4tJ9qkXIazAJIWaxxqwqJU beichen@M2800
    The key's randomart image is:
    +---[RSA 2048]----+
    |   oo+o..        |
    |. o +.o. .       |
    |.+ O +. ..       |
    |o E + o  .o .    |
    |.o O . oS... .   |
    |. o o o o.o o    |
    |     + o + + =   |
    |    . o +.o *    |
    |       . o++     |
    +----[SHA256]-----+

After this, type

    cd ~/.ssh/
    cat id_rsa.pub 
Copy the content into the authorized_keys in this repo, and commit it.

If you want to use the sshkey,

    git clone https://github.com/ECE4564-Group15/sshkey.git
    mkdir ~/.ssh
    mv ./sshkey/authorized_keys ~/.ssh
    
In this way everyone can get each other's sshkey, so we can ssh into ohter's rsp pi

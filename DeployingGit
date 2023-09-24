# Local Deployement

## Dependencies

1. SSH Server

Thing is git uses SSH under the hood to communicate with each other in case if ssh is not installed on either of your devices then it will not be able to communicate.

## PING GIT SERVER

```sh
ping <GIT_SERVER_IP>
```

## CHECKING IF SSH Server is install on window

1. Open Settings
2. Apps
3. Apps & features
4. On the right hand side, below **Apps & features** you can see the **Optional features**
5. Inside **Optional features**,  you can search the SSH and can see **OpenSSH Client** and **OpenSSH Server**.
6. In case, if they are not installed you can directly install them by clicking on **Add a feature** and searching **openssh client** and **openssh server** and clicking on **install** respectively.
7. To run **openssh server** on windows, Open **Services** and search **OpenSSH SSH Server** right click and Press **Start**.

> REMEMBER!
> OpenSSH CLient is used to login in to the other devices using SSH whereas OpenSSH Server allow other devices to logged into the device using SSH.

## SSH GIT SERVER

```sh
ssh "USER_NAME"@<IP_OF_MACHINE>
```

Make sure that the block isn't blocked by the firewall or the antivirus.

## Checking PORT

### LINUX/MAC

```sh
nc -zv <IP> <PORT>
```

### Window Powershell

```sh
(new-object Net.Sockets.TcpClient).Connect("<IP_OF_MACHINE", PORT)
```

If it returns no output it means that then PORT is accessible else port is blocked.

## CREATE REPOSITORY

You need to create a git repostiory on GIT SERVER.

```sh
git init
```

## HOSTING REPOSITORY ON WINDOW

```sh
git daemon --verbose --enable=upload-pack --enable=receive-pack --base-path-g:/ --export-all
```

[The `git clone git://` command uses the Git protocol, which by default operates over port 9418](https://serverfault.com/questions/189070/what-firewall-ports-need-to-be-open-to-allow-access-to-external-git-repositories)[1](https://serverfault.com/questions/189070/what-firewall-ports-need-to-be-open-to-allow-access-to-external-git-repositories)[2](https://www.w3docs.com/learn-git/git-clone.html). [This is a special daemon that provides a service similar to SSH but without any authentication](https://www.w3docs.com/learn-git/git-clone.html)[2](https://www.w3docs.com/learn-git/git-clone.html). 

> Disabling the firewall works for me.

### For above method you can clone as follow.

```sh
git clone git://192.168.0.110/<repository_name>
```

## CLONING GIT REPOSITROY

On client, you need to run the following command.

### LINUX

```sh
git clone "user_name"@IP:/path/to/repo
git clone "test"@192.168.0.100:/Users/test/
```

### WINDOW

```sh
Make sure that your c:/xampp/htdocs folder (or sub folders of it) is shared in windows, so you can navigate on the network by this address:

\\192.168.0.6\htdocs
Then you clone by using file:////. Note that there are four slashes:

git clone file:////192.168.0.6/htdocs/somerepo.git
```

```sh
https://stackoverflow.com/questions/5200181/how-to-git-clone-a-repo-in-windows-from-other-pc-within-the-lan
https://stackoverflow.com/questions/18813847/cannot-open-git-upload-pack-error-in-eclipse-when-cloning-or-pushing-git-repos
https://stackoverflow.com/questions/1483722/git-receive-pack-command-not-found-in-windows
https://stackoverflow.com/questions/11128464/git-upload-pack-command-not-found
https://stackoverflow.com/questions/50895265/git-upload-pack-command-not-found-on-windows-but-works-on-osx
```


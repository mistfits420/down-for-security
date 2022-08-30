---
title: "Executing Code From Server"
date: 2022-08-30T11:32:29+02:00
draft: false


cover:
    image: hacker.jpg
tags: ["Task"]

---

Sometimes we find ourself forgeting the most simple commands and having to learn them all over again. This sometimes can become anoying and even frustrating. Everyone forgets stuff and that's totally OK, but sometimes you find yourself in desperate need to type a commmand which you learned 1 week ago but now you can't even remember half of it, am i right? Today i'm gonna teach you how to have all the commands you need instanly ready without bothering to remember or EVEN TYPE THEM AT ALL.....yes you read that right you don't even need to type them at all.
<br></br>

Now you may be wondering how can i use the complicated commands i need to finish my job without even typing them at all? The way we're going to do this is by writing all the important commands on a online server then accessing them through our terminal just by calling the name of the command which you will set. So let's not waste time anymore and get straight into it.

<br></br>

* Step 1 is to write some commands on .txt files(every .txt file should an invidual command that does a specific task/job. You can't write two seperate commands that do seperate jobs). Here's an example:

![image](command-1.png)

on the image above i created a file called `1.txt` and then wrote the command: `ping google.com`.

* Step 2 is to create a bunch of .txt files with all the commands you need or long commands which are complicated and hard to remember

* Step 3 is to find a free hosting service, a great option is:

* `https://freewha.com/`

Go ahead and create a subdomain and chose a domain.(always choose something that's not complicated and you can write it easy and fast on your keyboard):

![image](subdomain.png)

on this case i created my server called `compp.orgfree.com`.

press proceed and you will be redirected to this page:
![image](account-1.png)

Enter any email account.(verification is not required). Aafter you entered the email and password, press "create" and that's it your domain is now ready to use. You will be redirected to a page that looks like this:
![image](blured-ftp.png)
Now we will need to upload our `1.txt` file which contains the command, so we need to look at the `Your Personal FTP Information` section. To login to the FTP server we will use FileZilla. It's easy to download, just open your terminal and type:
`sudo apt-get install filezilla`.
After the download is finished, type `filezilla` on your terminal and you should see something like this:
![image](filezilla.png)
Go on and fill all the information needed to login:

<br></br>
FTP Server/Host: > Host:

FTP Login/Username: > Username:

FTP PassWord > Password:

and for the `Port:` enter `21`. After you filled all the information press "Quickconnect". After you are connected to your server, on the right side on you should see these files:
![image](site-storage.png)
Go ahead and delete all of them except `ftpquota`.
Now drag your `1.txt` file there. You should see something like this:
![image](files.png)
Finally! Everything is now ready, just to be sure open a new google tab and search `yourdomain.com/1.txt`. This is how your command show be showing:
![image](command.png)
Finally open your terminal and type:

* `$(curl http://compp.orgfree.com/1.txt)`

![image](request-1.png)

As you can see on the image above, i request the command from my server to ping google. You can do this process with all the commands that you find hard and very complicated to memorize. Just make sure to write them in seperate files.(This has been tested only on Linux systems, no testings have been done on Windows or mac). After you have a server full of your precious commands all you have to do is to call them by name:

myserver.com/1.txt

myserver.com/network-scan.txt

myserver.com/open-port-22.txt

etc.

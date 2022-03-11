---
typora-copy-images-to: figure
---

# How to use Nikto

## 1. Install

The first thing is we need to install Nikto in the operating system. 

For windows user, the use of Nikto needs to rely on the Active State prel environment, so the Acticve State prel needs to be installed first. 

For Linux user, it will be easy. You can use the following commands to update the system and install the Nikto.[^intall_nikto]

```bash
sudo apt-get update 
sudo apt-get upgrade 
sudo apt-get install nikto -y
```



## 2. Function

After we installed the nikto, we can use the following command to check what function does nikto have. 

```bash
nikto -h
```

The result will show as the following figure. 

![574668f75a20b456935aa3d388a6580](figure/574668f75a20b456935aa3d388a6580.png)

More information can be found from the nikto repo in the Github  [^nikto_repo]or this website.[^this_website]

Let try one of these. 

```bash
nikto -list-plugins
```

It will list all available plugins which are shown in the following figure.

![2423b05191f244b6ce7734747c00bfe](figure/2423b05191f244b6ce7734747c00bfe.png)



## 3. basic scan

If we just want to do the basic scans of web pages, just use the following command:

```bash
nikto -h url/ip
```

where the "url/ip" can be the URL of the website or the IP address of the website, for example if we want to do a basic scan for the owl page, we can use:

```bash
nikto -h https://owl.uwo.ca/portal/site/~8d4444ef-07ac-4254-a254-24b6b55e039a/tool/bb31b258-3b6c-487e-9c8b-5ae873a6e916
```

or

```bash
nikto -h 129.100.0.33
```

Then the scan will start and the information will be displayed, as the following figure shows. 

The first block shows some information of the website such as IP address, Hostname and the port. the second block shows the SSL information and the third block shows the potential problems of this website. For example, it shows **_the cookie JSESSIONID created without the secure flag and the httponly flag, Xoops portal give detail error messages including SQL suntax and may allow an exploit, and  Web Wiz Forums ver. 7.01 and below is valnerable to Cross Site Scripting(XSS)._**

![42066538b7566c832628506fc0b2a2b](figure/42066538b7566c832628506fc0b2a2b.png)

![c5b1dfb8bdac4e9105ad6392dcf8bd8](figure/c5b1dfb8bdac4e9105ad6392dcf8bd8.png)



## 4. Assign the specific port and format the output

If we want to assign the specific port and format the output, we can use ```-p``` and ```-o``` in our command:

```bash
nikto -h url/ip -p port -o format
```

For example:

```bash
nikto -h https://owl.uwo.ca/portal/site/~8d4444ef-07ac-4254-a254-24b6b55e039a/tool/bb31b258-3b6c-487e-9c8b-5ae873a6e916 -p 443 -o uwo1.txt
```

The above example shows we assign the port 443 and we format the output in the uwo1.txt file. 

![6797f51ff11ab018421aeb1f31ece60](figure/6797f51ff11ab018421aeb1f31ece60-16469845062371.png)



## 5. Scan for multiple websites

If we want to scan for multiple websites, we can create a txt file and put the URL of these websites line by line:

![91de8113be766eef11c66bc82c09396](figure/91de8113be766eef11c66bc82c09396.png)

Then using this command will let it scan these websites from bottom to the top.

```bash
nikto -h xxxx.txt
```

Where xxxx.txt in our example is 1234.txt. 

![0d8243db605d7dc2615f7d968b728a4](figure/0d8243db605d7dc2615f7d968b728a4.png)



## 6. Scan with the specific method

The Nikto offer a tuning function which allows us to specific the scan method. The detail can be found in [this website](https://www.mankier.com/1/nikto). 

We can use ```-T number``` in the command to use this function. For example:

```bash
nikto -h https://owl.uwo.ca/portal/site/~8d4444ef-07ac-4254-a254-24b6b55e039a/tool/bb31b258-3b6c-487e-9c8b-5ae873a6e916 -T 35
```

This example shows the result of scanning the owl website with "3. Information Disclosure" and "5. Remote File Retrieval - Inside Web Root". And the processing time of this scan is extremely fast which is just 10 seconds. 

![7c47320698542f907e268096df6c30d](figure/7c47320698542f907e268096df6c30d.png)



## 7. other commands

In addition to the examples we show, the Nikto also offers a lot of functions such as ```-findonly```, ```-ssl```, ```-useproxy``` etc. for different situations. We can choose the appropriate functions to accomplish our task in different situations





# Reference

[^intall_nikto]: https://linuxhint.com/install_nikto_ubuntu/.
[^nikto_repo]: https://github.com/sullo/nikto/wiki.
[^this_website]: https://www.mankier.com/1/nikto.
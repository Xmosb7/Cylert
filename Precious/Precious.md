at the first i used nmap

![](./1.png)

so let’s open it in the browser

![](./2.png)

it’s a page which take a url then take screenshot then convert it to pdf file

let’s try the functionality and see what the file

![](./3.png)

just search for CVE in the creator tool

and i found there command injection vulnerability

[Command Injection in pdfkit | CVE-2022-25765 | Snyk](https://security.snyk.io/vuln/SNYK-RUBY-PDFKIT-2869795)

![](./4.png)

there is command injection

know we can make sure of it

![](./5.png)

![](./6.png)

let’s make reverse shell

![](./7.png)

after some enumeration and searching we found this file in the user directory

![](./8.png)

it’s a folder which has some configurations

![](./9.png)

now how esclate

when we did some enumeration we found there ruby file can run with sudo without password

![](./10.png)

and when we run it and understand the file we found it do some updates from serialized YML file but the idea here , the file read *dependencies.yml* file from the current shell directory

![](./11.png)

here we need to create this file then inject our payloads to it

![](./12.png)

we can create this file in the ***tmp*** directory and open listner from our local machine

![](./13.png)

![](./14.png)

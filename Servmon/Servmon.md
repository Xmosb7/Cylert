let’s start with nmap

![](./1.png)

FTP time

using anonymous user

![](./2.png)

with some searching

![](./3.png)

![](./4.png)

after open the ip http page we found this TVT NVMS 1000 which has directory traversal so let’s try nathan desktop

![](./5.png)

we get win.ini file so let’s go to */Users/Nathan/Desktop/Password.txt*

![](./6.png)

will try it in ssh

we will try password spray in ssh using metaploit

![](./7.png)

logged successfully with nadine and one pass of the previous
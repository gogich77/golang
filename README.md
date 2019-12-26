# How to update the Go version

System: Lunux

### 1. Find your and the last avalable version. 

```
$ go version
go version go1.13.4 linux/amd64
```
https://golang.org/dl/

### 2. Locate the working go installation folder
In case the go is instaleld and works find it like that  
Use where is to find the 
```
$ whereis go
go: /usr/local/go /usr/local/go/bin/go
```
### 2. Download the new version

Take the URL link from https://golang.org/dl/
```
wget https://dl.google.com/go/go1.13.5.linux-amd64.tar.gz
```

### 3. Install it
```
$ tar -xzf go1.13.5.linux-amd64.tar.gz
```
This will make a local go folder.

```
# mv /usr/local/go /usr/local/go-old
```
Root is needed. Move the old working go folder

```
# mv ./go /usr/local/go
```
Move the local new go folder to the old place

```
# chown root:root -r  /usr/local/go
```
The owner has to be the root

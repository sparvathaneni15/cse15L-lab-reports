# Week 7 Lab Report

## Samanyu Parvathaneni

### **PART 1**

### Changing the name of the `start` parameter and its uses to `base`

After accessing the file with vim by entering `vim DocSearchServer.java`, I was met with this screen.

![image](./Before.png)


In order to replace all appearances of the string `start` with `base`, I entered the following vim command:

`:%s/start/base/gc<Enter>`

![image](./During.png)

This single command replaces all instances of the string `start` with `base`

![image](./After.png)

### **PART 2**

Using Visual Studio Code, it took about 30 seconds. It took me a few minutes to recollect how to properly `scp` the edited file into the remote server.

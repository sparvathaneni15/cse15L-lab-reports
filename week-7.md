# Week 7 Lab Report

## Samanyu Parvathaneni

### **PART 1**

### Changing the name of the `start` parameter and its uses to `base`

After accessing the file with vim by entering `vim DocSearchServer.java`, I was met with this screen.

![image](./Original.png)


In order to replace all relevant appearances of the string `start` with `base`, I entered the following vim command:

`:%s/start/base/gc<Enter>`

![image](./Before.png)

After hitting enter, the terminal prompts me to change the highlighted string by entering `y` or `n`.

![image](./Change1.png)

After hitting `y`, the highlighted instance is replaced and the program moves on to the next instance of `start` and prompts the same thing.

![image](./Change2.png)

![image](./Change3.png)

Once it got to an instance of `start` that I did not want to change, I entered `n`.

![image](./Change4.png)

Finally, the vim command is done running and the desired changes have been made.

![image](./After.png)

![image](./LastPart.png)

### **PART 2**

Using Visual Studio Code, it took about 30 seconds. It took me a few minutes to recollect how to properly `scp` the edited file into the remote server.

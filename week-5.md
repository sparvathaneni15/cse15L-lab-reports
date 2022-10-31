# Week 5 Lab Report

## Samanyu Parvathaneni

### ```less```

```
less -m ./*/*.txt
```

![image](./Command1-Example1.png)
The `-m` option provides a progress tracker at the bottom that tells the user what percentage of the file they have read through. This is useful because it tells the user how much of the file they have left to read, relative to how much they have already read.

```
less -M ./*/*.txt
```

![image](./Command1-Example2.png)
The `-M` option includes what lines are being displayed on the terminal screen out of how many lines there are, and the percentage read through. This is more useful than the previous option because it displays the total amount of lines left to read, not just the percentage.

```
less -N ./*/*.txt
```

![image](./Command1-Example3.png)
The `-N` option adds the line number of each line to the beginning of each line. This is useful because it is easier to find a specific line if the line number is displayed at the beginning of each line.


### ```find```

```
find -s ./*/
```

![image](./Command2-Example1.png)
The `-s` option lists the directories and file paths lexographically (alphabetical within each directory). This is useful because it organizes the file paths in a way that the user is most likely familiar with, making it easier to search through.

```
find -d ./*/
```

![image](./Command2-Example2.png)
The `-d` option causes the output to be listed after a depth-first traversal has been made. This is useful because it gives the user freedom to return the output in a certain format.

```
find -x ./*/
```

![image](./Command2-Example3.png)
The `-x` option prevents find from calling the command on the returned directories that have a device number different than that of the file from which the descent began. This is useful because it makes sure that the command is called on files and directories that are actually in the directory `find` was called on.


### ```grep```

```
grep -L terrorism ./*/*
```

![image](./Command3-Example1.png)
The `-L` option outputs all of the file names that do not have the passed argument in its contents. This is useful because it may be necessary for your purposes to know which files do not contain a certain string argument.

```
grep -b biology ./*/*
```

![image](./Command3-Example2.png)
The `-b` option displays the offset in bytes of a matched pattern after file path. This is useful because it tells the user how far after the beginning of the line the argument is found in the line.

```
grep -n cells ./*/*
```

![image](./Command3-Example3.png)
The `-n` option displayes the line number of each line that contained the passed argument. This is useful because it tells the user where in the file the passed argument can be found.

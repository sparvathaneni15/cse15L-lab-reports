# Week 5 Lab Report

## Samanyu Parvathaneni

### ```less```

```
less -m ./*/*.txt
```

![image](./Command1-Example1.png)
The `-m` option provides a progress tracker at the bottom that tells the user what percentage of the file they have read through.

```
less -M ./*/*.txt
```

![image](./Command1-Example2.png)
The `-M` option provides an even more functional version of the previous command option. This one includes what lines are being displayed on the terminal screen out of how many lines there are, and this one includes the percentage read through.

```
less -N ./*/*.txt
```

![image](./Command1-Example3.png)
The `-N` option adds the line number of each line to the beginning of each line.


### ```find```

```
find -s ./*/
```

![image](./Command2-Example1.png)
The `-s` option lists the directories and file paths lexographically (alphabetical within each directory).

```
find -d ./*/
```

![image](./Command2-Example2.png)
The `-d` option causes the output to be listed after a depth-first traversal has been made.

```
find -x ./*/
```

![image](./Command2-Example3.png)
The `-x` option prevents find from calling the command on the returned directories that have a device number different than that of the file from which the descent began.


### ```grep```

```
grep -L terrorism ./*/*
```

![image](./Command3-Example1.png)
The `-L` option outputs all of the file names that do not have the passed argument in its contents.

```
grep -b biology ./*/*
```

![image](./Command3-Example2.png)
The `-b` option displays the offset in bytes of a matched pattern after file path.

```
grep -n cells ./*/*
```

![image](./Command3-Example3.png)

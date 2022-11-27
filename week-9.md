# Week 7 Lab Report

## Samanyu Parvathaneni

### Code Block

```
# Create your grading script here

#set -e

CPATH=".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar:student-submission/"

rm -rf student-submission
git clone $1 student-submission

if [[ -f student-submission/ListExamples.java ]]
then
    echo $?
else
    echo "ListExamples.java doesn't exist"
    echo "score: 0"
    exit 1
fi

touch student-submission/ListExamples.java
mv student-submission/ListExamples.java .

javac -cp $CPATH TestListExamples.java 2>compError.txt

if [[ $? -eq 0 ]]
then
    echo "compile success"
else
    echo "compile failed"
    cat compError.txt
    echo "score: 0"
    exit 1
fi 

java -cp $CPATH org.junit.runner.JUnitCore TestListExamples 1>codeError.txt
cat codeError.txt


#NUMBEROFERROR= grep -o "E" codeError.txt|wc -l how to minus in sh?
#echo 2-$NUMBEROFERROR
```

# Week 7 Lab Report

## Samanyu Parvathaneni

### Code Block

```
rm -rf student-submission
git clone $1 student-submission
if [[ -f ./student-submission/ListExamples.java ]]
then
    cp ./student-submission/ListExamples.java .
    javac -cp .:./lib/hamcrest-core-1.3.jar:./lib/junit-4.13.2.jar *.java 2> output-error.txt
    if [[ -s output-error.txt ]]
    then
        echo "The submitted file does not compile."
        cat output-error.txt
        echo "Fail"
        exit
    else
        echo "Compile Successful!"
        java -cp .:./lib/hamcrest-core-1.3.jar:./lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
    fi
else
    echo "Submission did not contain the required file"
    echo "Fail"
    exit
fi
```

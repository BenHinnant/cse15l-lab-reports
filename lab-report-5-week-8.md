# lab-report-5-week-8.md

# Grade.sh
## Made partly in collaboration with Andrew Pan
```
set -e
 
rm -rf student-submission
git clone $1 student-submission
cd student-submission
 
FILE=./ListExamples.java
if test -f "$FILE" ;
then
    echo "$FILE exists."
else
    echo "$FILE does not exist in this directory or is not a regular file."
    echo "Grade: 2/10"
    exit 1
fi
 
mkdir -p ./testdir
cp ./ListExamples.java ./testdir
cp ../TestListExamples.java ./testdir
 
cd ./testdir
set +e
javac -cp ".;../../lib/hamcrest-core-1.3.jar;../../lib/junit-4.13.2.jar" *.java
if [ $? -eq 0 ]
then
    echo "Compiled Successfully."
else
    echo "Did not Compile Successfully."
    echo "Grade: 5/10"
    exit 1
fi
 
java -cp ".;../../lib/hamcrest-core-1.3.jar;../../lib/junit-4.13.2.jar" org.junit.runner.JUnitCore TestListExamples
if [ $? -eq 0 ]
then
    echo "Java Ran Successfully."
    echo "Grade: 10/10"
else
    echo "Java did not run Successfully."
    echo "Grade: 7/10"
fi
```

# list-methods-corrected

![image](https://user-images.githubusercontent.com/55713184/204061213-be85a597-c7ca-4801-a347-1a5a22ec5a13.png)

![image](https://user-images.githubusercontent.com/55713184/204061283-0dc82a9c-69bb-4ac5-87e4-74ee1be56ff8.png)


# list-methods-compile-error

![image](https://user-images.githubusercontent.com/55713184/204061231-055ae69c-2d9a-4e41-bc91-91f0a03f9ed4.png)

![image](https://user-images.githubusercontent.com/55713184/204061306-bb51a2ec-b977-4a8a-9c8d-ff7d22ba5a21.png)

# list-methods-filename

![image](https://user-images.githubusercontent.com/55713184/204061245-0235ee11-da92-4525-b3c0-44173ccbb863.png)

![image](https://user-images.githubusercontent.com/55713184/204061323-37e2e7e3-e09e-4940-9149-0e69ffaf46b4.png)

## Trace for browser interface
```
set -e  //stdout: none  stderr: none  return code: 0
 
rm -rf student-submission //stdout: none  stderr: none  return code: 0
git clone $1 student-submission //stdout: "Cloning into 'student-submission'..."  stderr: none  return code: 0
cd student-submission //stdout: none  stderr: none  return code: 0
 
FILE=./ListExamples.java  //stdout: none  stderr: none  return code: 0
if test -f "$FILE" ;  //condition is false because their submitted file is not ./ListExamples.java, 
                      //so the command will not be able to check the file type of ./ListExamples.java
then  //Does not run
    echo "$FILE exists."  //Does not run
else  //stdout: none  stderr: none  return code: 0
    echo "$FILE does not exist in this directory or is not a regular file." //stdout: "$FILE does not exist in this directory or is not a regular file."
                                                                            //stderr: none  return code: 0
    echo "Grade: 2/10"  //stdout: "Grade: 2/10" stderr: none  return code: 0
    exit 1  //stdout: none  stderr: none  return code: 1
fi  //Does not run
 
mkdir -p ./testdir  //Does not run
cp ./ListExamples.java ./testdir  //Does not run
cp ../TestListExamples.java ./testdir //Does not run
 
cd ./testdir  //Does not run
set +e  //Does not run
javac -cp ".;../../lib/hamcrest-core-1.3.jar;../../lib/junit-4.13.2.jar" *.java //Does not run
if [ $? -eq 0 ] //Does not run
then  //Does not run
    echo "Compiled Successfully." //Does not run
else  //Does not run
    echo "Did not Compile Successfully."  //Does not run
    echo "Grade: 5/10"  //Does not run
    exit 1  //Does not run
fi  //Does not run
 
java -cp ".;../../lib/hamcrest-core-1.3.jar;../../lib/junit-4.13.2.jar" org.junit.runner.JUnitCore TestListExamples //Does not run
if [ $? -eq 0 ] //Does not run
then  //Does not run
    echo "Java Ran Successfully." //Does not run
    echo "Grade: 10/10" //Does not run
else  //Does not run
    echo "Java did not run Successfully." //Does not run
    echo "Grade: 7/10"  //Does not run
fi  //Does not run
```








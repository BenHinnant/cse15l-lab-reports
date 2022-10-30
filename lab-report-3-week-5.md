# find Windows Command Line Options

## /v Switch

### Example 1: find /v "flight" "technical\911report\chapter-1.txt"

![image](https://user-images.githubusercontent.com/55713184/198896209-5f349a0e-76e9-4735-828f-c6befe63a1aa.png)

* This command prints all lines not containing the string "flight" within the chapter-1.txt file. By excluding lines with "flight" using the /v switch, the user might be able to find information related to the situation on the ground during 9/11.

### Example 2: find /v "Fig" "technical\biomed\1471-213X-1-11.txt" 

![image](https://user-images.githubusercontent.com/55713184/198897006-ec8ce0fb-8d0a-4287-bc76-0398c86ba374.png)

* This command prints all lines not containing the string "Fig" within the chapter-1.txt file. By excluding lines with "Fig" using the /v switch, the user might be able to find information that is not related to a figure within the file.

### Example 3: find /v "recommendation" "technical\government\Alcohol_Problems\DraftRecom-PDF.txt" 

![image](https://user-images.githubusercontent.com/55713184/198897517-c75690fe-3fa3-49d1-aa74-15b551322183.png)

* This command prints all lines not containing the string "recommendation" within the chapter-1.txt file. By excluding lines with "recommendation" using the /v switch, the user might be able to find background information that is not related to the committee's recommendations within the file.

## /i Switch

### Example 1: find /i "recommendation" "technical\government\Alcohol_Problems\*.txt" 

![image](https://user-images.githubusercontent.com/55713184/198897842-c545f3ec-c290-4616-a847-10923d50182e.png)
![image](https://user-images.githubusercontent.com/55713184/198897864-583e094e-9b83-46af-bfe0-30e50c6b7352.png)

* This command prints all lines containing the string "recommendation" regardless of capitalization within all text files contained in the Alcohol_Problems directory. This might be used as a rough estimate to determine which text file has the most recommendations.

### Example 2: find /i "situation" "technical/911report/chapter-10.txt"

![image](https://user-images.githubusercontent.com/55713184/198898400-29506b0a-8f6f-46f1-8e7f-f51ed1c7db6b.png)

* This command prints all lines containing the string "situation" regardless of capitalization within chapter-10.txt. This allows the user to find lines related to the situation during 9/11 as well as the White House Situation Room.

### Example 3: find /i "situation" "technical/911report/\*.txt"

![image](https://user-images.githubusercontent.com/55713184/198899199-9a6fe984-d5ea-4b32-82dc-10138ef67eed.png)
![image](https://user-images.githubusercontent.com/55713184/198899213-62804c39-f596-46f3-95c2-b554deda90fe.png)

* This command prints all lines containing the string "situation" regardless of capitalization within all text files contained in the 911report directory. This allows the user to find lines related to the situation during 9/11 as well as the White House Situation Room across multiple files. 

## /c Switch

### Example 1: find /c "Clinton" "technical/911report/\*.txt"   

![image](https://user-images.githubusercontent.com/55713184/198906731-e5b89f80-cbca-4d01-82d4-6a3b42d60aae.png)

* This command prints the number of times the string "Clinton" appeared in each .txt file of the 911report directory. This allows the user to easily determine which files often mention the president.

### Example 2: find /c "recommendation" "technical/government/alcohol_problems/\*.txt"

![image](https://user-images.githubusercontent.com/55713184/198907250-91b04cf1-31be-452d-b907-5a9a249b9dd2.png)

* This command prints the number of times the string "recommendation" appeared in each .txt file of the Alcohol_Problems directory. This allows the user to easily determine which files have the most recommendations.

### Example 3: find /v /c "meth" "technical/government/Env_Prot_Agen/\*.txt"

![image](https://user-images.githubusercontent.com/55713184/198907201-dd68c42c-18bd-4d91-98ec-dad6dfe1cdb7.png)

* This command displays a count of the lines that don't contain the String "meth" for all .txt files in the Env_Prot_Agen directory. This is a rough approximation of the number of times the string "meth" was mentioned for each file.





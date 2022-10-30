# find Windows Command Line Options

## /v Switch

### Example 1: find /v "flight" "technical\911report\chapter-1.txt"

![image](https://user-images.githubusercontent.com/55713184/198896209-5f349a0e-76e9-4735-828f-c6befe63a1aa.png)

* This command prints all lines not containing the string "flight" within the chapter-1.txt file. By excluding lines with "flight" uisng the /v switch, the user might be able to find information related to the situation on the ground during 9/11.

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



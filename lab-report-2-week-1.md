# Installing VScode
* Already had VScode downloaded on laptop
* To download, follow instructions on their website

![Image](https://lh3.googleusercontent.com/keep-bbsk/AP6BvTTnK3abTbXeAbsYBrscQXUyyLqL4MG38mbn8lBxETK0LcJ3lo3wZOg8neHfdXwdUjAoqwf2KRDuZPJ4P3soPJ1p3BRPK4xxgguvEsrBahTxRfSV=s1600)

# Remotely Connecting
* Reset password on course-specific account during lab, but the password failed to work; the terminal kept prompting me for the password again until it closed the connection with the server
* Tried resetting my password the next day and it worked after 15 mins

![image](https://user-images.githubusercontent.com/55713184/193392159-401237dd-f72c-40b5-a368-310fee10170b.png)

# Trying Some Commands
* Ran several commands on my Windows client and the Linux server to understand their functionality
* I had a Windows computer so Linux commands like ls and cp failed to work

![image](https://user-images.githubusercontent.com/55713184/193391095-adf8c448-bdb9-45f7-b625-0af19aba82d3.png)
![image](https://user-images.githubusercontent.com/55713184/193392185-ff41a838-4043-4a37-953e-682f7cb3733d.png)

# Moving Files with scp
* Create a file named WhereAmI.java, copy it into the server using scp, access the server using ssh, and run the file using javac and java commands
* The javac command creates the class file that java command runs
* I did not run javac and java on my computer because I haven't downloaded java yet

![image](https://user-images.githubusercontent.com/55713184/193392657-86605858-0bcb-4e6a-b258-bb3a989f1127.png)

# Setting an SSH Key
* Create public and private ssh keys using ssh-keygen
* Then use ssh mkdir and scp to add the public key to a .ssh directory on the server
* You can now access the server without entering the password

![image](https://user-images.githubusercontent.com/55713184/193392763-93fe6372-a297-41d0-9ca2-090aff86e35d.png)

# Optimizing Remote Running
* I tried running “scp WhereAmI.java cs15lfa22li@ieng6.ucsd.edu:~/; ssh cs15lfa22li@ieng6.ucsd.edu; javac WhereAmI.java; java WhereAmI” but the terminal outputs: “WhereAmI: No such file or directory” although WhereAmI.java exists in my client home folder and remote home folder
* I tried various other combinations of quotations and colons with roughly the same output
* The only difference was a quotation mark at the end of the file name: <WhereAmI.java”: No such file or directory>

![image](https://user-images.githubusercontent.com/55713184/193393010-8d79c314-9691-4a75-8a72-6010f03d2d9d.png)
![image](https://user-images.githubusercontent.com/55713184/193392986-b507f1d0-943c-429b-9489-474a45e25dea.png)

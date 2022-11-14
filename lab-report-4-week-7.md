# lab-report-4-week-7.md

# Part 1

## Adding a new line to print before File[] paths = f.listfiles()

```
vim d<Tab><Enter>17ggo<Shift>sy<Ctrl>n.out.pr<Ctrl>n<Shift>9'dir=<Shift>'+f.to<Shift>S<Ctrl>n<Shift>900;<Esc>:wq<Enter>
```

### Explanation of commands
```
vim d<Tab><Enter>
```
![image](https://user-images.githubusercontent.com/55713184/201541745-1783730a-8aee-471c-a8d7-60e14e48fb5f.png)
![image](https://user-images.githubusercontent.com/55713184/201540027-1004a5de-0dbd-485c-aa7d-571da1683294.png)

* This command opens DocSearchServer.java by autocompleting the file name using the tab key.

```
17gg
```
![image](https://user-images.githubusercontent.com/55713184/201540159-8f535247-d625-40c9-b2e6-e85d7b1e5bc0.png)

* This command moves the cursor to the beginning of line 17.

```
o
```
![image](https://user-images.githubusercontent.com/55713184/201540641-73a15c30-83b3-4e10-8c76-54a6d34e990b.png)

* This command inserts a new line below the current line.

```
<Shift>sy<Ctrl>n.out.pr<Ctrl>n<Shift>9'dir=<Shift>'+f.to<Shift>S<Ctrl>n<Shift>900;
```
![image](https://user-images.githubusercontent.com/55713184/201541460-f3d0b0f3-4495-4a70-9fa0-44f3d79611d6.png)

* This command adds a line to the program that will print out a statement designating File f as a directory. It uses autocomplete to reduce keystrokes.

```
:w<Enter>
```

![image](https://user-images.githubusercontent.com/55713184/201545746-552b380c-82a5-458f-9f35-262c4b1009e6.png)

* This command saves the file.

# Part 2

* Making the edit in visual studio code: Took 3 minutes 34 seconds, mostly due to file transfer time
* Starting already logged into a ssh session: Took 1 minute 18 seconds
* I would prefer to use the second method because I don't have to deal with the long file transfer time. I also wouldn't need to ssh and scp back and forth between my computer and the remote server. If it is my first time moving the project's files to the remote computer, I would use the first method because I'll have to deal with the long file transfer time anyways. If unedited files are already on the remote, I will use the second method to save time from not needing to do ssh and scp.

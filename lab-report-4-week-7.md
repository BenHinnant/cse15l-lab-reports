# lab-report-4-week-7.md

# Part 1

## Adding a new line to print before File[] paths = f.listfiles()

```
vim d<Tab><Tab><Enter>
17gg<Enter>
o<Enter>
<Shift>sy<Ctrl>n.out.pr<Ctrl>n<Shift>9'd=<Shift>'+f.to<Shift>S<Ctrl>n<Shift>900;
<Esc>
:wq<Enter>
```

### Explanation of commands
```
vim d<Tab><Tab><Enter>
```
![image](https://user-images.githubusercontent.com/55713184/201540027-1004a5de-0dbd-485c-aa7d-571da1683294.png)

* This command opens DocSearchServer.java by autocompleting the file name using the tab key. If the class file exists as well, it may be necessary to press tab twice.

```
17gg<Enter>
```
![image](https://user-images.githubusercontent.com/55713184/201540159-8f535247-d625-40c9-b2e6-e85d7b1e5bc0.png)

* This command moves the cursor to the beginning of line 17.

```
o<Enter>
```
![image](https://user-images.githubusercontent.com/55713184/201540641-73a15c30-83b3-4e10-8c76-54a6d34e990b.png)

* This command inserts a new line below the current line.


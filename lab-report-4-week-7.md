# Part 1

## Adding a new line to print before File[] paths = f.listfiles()

```
vim d<Tab><Tab><Enter>
17G <Enter>
<Shift> + O <Enter>
System.out.println("Directory: " + f.toString()); <Enter>
<Esc>
:wq <Enter>
```

### Explanation of commands

vim d<Tab><Tab><Enter>

![image](https://user-images.githubusercontent.com/55713184/201540027-1004a5de-0dbd-485c-aa7d-571da1683294.png)

* This command opens DocSearchServer.java by autocompleting the file name using the tab key. If the class file exists as well, it may be necessary to press tab twice.


17G <Enter>

![image](https://user-images.githubusercontent.com/55713184/201540159-8f535247-d625-40c9-b2e6-e85d7b1e5bc0.png)

* This command moves the cursor to the beginning of line 17.

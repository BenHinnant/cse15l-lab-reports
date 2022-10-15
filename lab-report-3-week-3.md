# Part 1

* Code for SearchEngine.java:

    import java.io.IOException;
    import java.net.URI;
    import java.util.ArrayList;

    class Handler implements URLHandler {
        // The one bit of state on the server: a number that will be manipulated by
        // various requests.
        ArrayList<String> strings = new ArrayList<String>();

        public String handleRequest(URI url) {
            if (url.getPath().equals("/")) {
                return String.format("Welcome to Ben's Server");
            } else if (url.getPath().equals("/search")) {
                String[] parameters = url.getQuery().split("=");
                    if (parameters[0].equals("s")) {
                        ArrayList<String> substrings = new ArrayList<String>();
                        for (String str:strings){
                            if (str.contains(parameters[1].toString())){
                                substrings.add(str);
                            }  
                        }
                        return substrings.toString();
                    }
            } else if (url.getPath().equals("/add")) {
                String[] parameters = url.getQuery().split("=");
                    if (parameters[0].equals("s")) {
                        strings.add(parameters[1].toString());
                        return String.format("Strings increased by 1!");
                    }
            } else {
                return "404 Not Found!";
            }
            return null;
        }
    }

    class SearchEngine {
        public static void main(String[] args) throws IOException {
            if(args.length == 0){
                System.out.println("Missing port number! Try any number between 1024 to 49151");
                return;
            }

            int port = Integer.parseInt(args[0]);

            Server.start(port, new Handler());
        }
    }

   
  
* Root directory:
  
![image](https://user-images.githubusercontent.com/55713184/195969906-8777b03c-4598-4a9a-9b8b-23866471347a.png)  

* 

# Part 2

## Bug 1: reverseInPlace in ArrayExamples.java

* The failure-inducing input:

![image](reverseInPlaceinp1.png)

* The symptom:

![image](reverseInPlacesym1.png)
![image](reverseInPlacesym2.png)
![image](reverseInPlacesym3.png)

* The bug:

![image](https://user-images.githubusercontent.com/55713184/195968651-c5da3398-769e-4011-b790-a5c9b0b0072a.png)

* The code after the bug was fixed:

![image](reverseInPlacefix1.png)

* Connection between the symptom and the bug:

The bug occurs because the function overwrites the index value while replacing it with an index value from the opposite end of the array. Since the index value is overriden without being stored elsewhere first, the function will return a palindromic array that is incorrect. However as shown in my tests, input arrays with lengths of 1 are unaffected since their sole index will not be overriden.

## Bug 2: filter in ListExamples.java

* The failure-inducing input:

![image](https://user-images.githubusercontent.com/55713184/195968948-d449b860-04ec-4450-8646-b57c115b4415.png)

* The symptom:

![image](https://user-images.githubusercontent.com/55713184/195969564-b6acb358-5e84-46aa-a347-6a64c5f7e90c.png)

* The bug:

![image](https://user-images.githubusercontent.com/55713184/195968899-1b1f2ebd-2762-4a8e-a26e-1bf0b22e56d3.png)

* The code after the bug was fixed:

![image](https://user-images.githubusercontent.com/55713184/195968995-2d1971a4-408b-426a-ac60-b22221998d98.png)

* Connection between the symptom and the bug:

The bug occurs because the function always adds the string to the first index of the list. When new elements are added to the list, older elements are pushed back by an index, so the list will be in reverse order from the order in which elements are added. As shown, input lists with one element are unaffected by the bug because there are no other elements to push back an index.

```
import java.net.URI;
import java.util.ArrayList;
import java.io.IOException;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.k
    String[] list = new String[100];
    ArrayList<String> strings = new ArrayList<>();


    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Strings: " + strings.toString());
        } 
        else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] parameters1 = url.getQuery().split("=");
                if (parameters1[0].equals("s")) {
                    strings.add(parameters1[1]);
                    return String.format("String added: " + "\"" + parameters1[1] + "\"");
                }
            }

            if (url.getPath().contains("/search")){
                String[] parameters2 = url.getQuery().split("=");
                ArrayList<String> query = new ArrayList<>();
                if (parameters2[0].equals("s")){
                    for (int j = 0; j < strings.size(); j++){
                        query.add(strings.get(j));
                    }
                    return String.format("Searched for strings: " + query.toString());
                }
            }
            return "404 not found";
        }
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
```

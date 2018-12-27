## HTTP Responses

> This file to define the codes indication which will be returned within the APIs   

```
  PS : Please be noted that "msg" attribute describe the meaning of code not the message we will send within the APIs .
  We can change the messages in "msg" attribute as the agreement between Backend and Mobile team
```

#### Informational Status

  - Codes between 100 to 199 used for sending an information between the server and client , preferred to be used under experimental conditions
    - **100 - Continue**
    ```
      {
        "code" : 100,
        "msg"  : "Continue",
        "explain"  : "Designed to utilize network bandwidth more efficiently by allowing servers an opportunity to confirm their readiness to accept large requests"
      }
    ```

#### Success Status

  - Codes between 200 to 299 indicate that everything works successfully

    - **200 - OK**
    ```
      {
        "code" : 200,
        "msg"  : "Ok",
        "explain"  : "Server processed the request successfully and transmitted content to the browser"
      }
    ```

    - **204 - No Content**
    ```
      {
        "code" : 204,
        "msg"  : "No Content",
        "explain"  : "Server sends a valid reply to client request that contains header information only and not contains any message body"
      }
    ```

#### Redirection Status

  - Codes between 300 to 399 indicate that we have redirection issue

    - **301 - Moved Permanently**

      ```
        {
          "code" : "301",
          "msg"  : "Moved Permanently",
          "explain"  : "indicates the URI specified by the client has been moved to a different location using a method called HTTP redirect, which allows the client to issue a new request and fetch the resource from the new location"
        }
      ```
    - **302 - Found**
      ```
        {
          "code" : "302",
          "msg"  : "Found",
          "explain"  : "a resource is moved temporarily rather than permanently , should be used only during brief content maintenance periods"
        }
      ```

    - **307 - Moved Temporarily**
      ```
        {
          "code" : "307",
          "msg" : "Moved Temporarily"
          "explain"  : "indicates temporary redirects"
        }
      ```

#### Client Errors

  - Codes between 400 to 499 indicate that the request for a web page or other resource contains bad syntax or cannot be filled for some other reason, presumably by fault of the client

    - **400 - Bad Request**

      ```
        {
          "code" : "400",
          "msg"  : "Bad Request",
          "explain"  : "the web server didn't understand the request because of invalid syntax"
        }
      ```
    - **401 - Unauthorized**
      ```
        {
          "code" : "401",
          "msg"  : "Unauthorized",
          "explain"  : "web client requests a protected resource on the server, but the client has not been authenticated for access"
        }
      ```

    - **403 - Forbidden**
      ```
        {
          "code" : "403",
          "msg"  : "Forbidden",
          "explain"  : "means that accessing the page or resource you were trying to reach is absolutely forbidden for some reason"
        }
      ```

    - **404 - Not Found**
      ```
        {
          "code" : "404",
          "msg"  : "Not Found",
          "explain"  : "the web server could not find the requested page, file, or ​another resource"
        }
      ```
      
      
    - **405 - Method Not Allowed**
      ```
        {
          "code" : "405",
          "msg"  : "Method Not Allowed",
          "explain"  : "the request method is known by the server but is not supported by the target resource."
        }
      ```

#### Server Errors

  - Codes between 500 to 599 indicate that the request for a web page or other resource in understood by the server but the server is incapable of filling the request for some reason

      - **500 - Internal Server Error**

        ```
          {
            "code" : "500",
            "msg"  : "Internal Server Error",
            "explain"  : "the web server received a valid request from a client but was unable to process it"
          }
        ```
      - **502 - Bad Gateway**
        ```
          {
            "code" : "502",
            "msg"  : "Bad Gateway",
            "explain"  : "A network issue between the client and server  can be triggered by configuration errors on a network firewall, router, or other network gateway device"
          }
        ```

      - **503 - Service Unavailable**
        ```
          {
            "code" : "503",
            "msg"  : "Service Unavailable",
            "explain"  : "indicates a web server cannot process the incoming client request"
          }
        ```

      - **504 - Gateway Timeout**
        ```
          {
            "code" : "504",
            "msg"  : "Gateway Timeout",
            "explain"  : "one of servers did not receive a timely response from another server that it was accessing while attempting to load the web page or fill another request by the browser"
          }
        ```

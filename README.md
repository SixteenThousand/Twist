## Twist

This is just a very basic wrapper around cURL that lets you make HTTP 
requests and have the output be printed in a relatively nice way, with 
syntax highlighting & automatic indentation of JSON output.

### Usage
```
twist [OPTIONS] [HTTP_METHOD] [URL] [[-s | --send] REQUEST_BODY_FILE]

Uses curl to send a http request. URL is the url to send the request to,
& HTTP_METHOD is the http method (GET,POST,PATCH,etc.) to use.
Use the --send/-s option to specify a request body from a file. The file 
must be in JSON format.

OPTIONS:
-t | --body-type : the format of the response body. Defaults to JSON.
-m | --header-output : The name of a file in which to dump the received
    header data. If unspecified, dumps it into a temporary file.
-o | --body-output : The name of a file in which to dump the received
    header data. If unspecified, dumps it into a temporary file.
```

### Dependencies
- fish (it's literally written in fish script)
- bat
- jq

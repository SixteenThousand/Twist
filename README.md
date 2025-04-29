# Twist

This is a little wrapper around [curl](https://curl.se/) I wrote in one 
evening that lets you make HTTP requests and have the output be printed in a 
relatively nice way, with syntax highlighting & automatic indentation of 
JSON output.

Since writing it, I've learned to just use curl; it's fine, I just wanted it 
to be simpler when I first started using it. This repository is not 
maintained any more, but is left public for anyone who might be interested.

## Usage
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
-v | --version : print version information
```

## Dependencies
- fish (twist is just an executable fish script)
- bat
- jq

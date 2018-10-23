
### Requirements

* JQuery
* bootstrap.js
* bootstrap.css

### Install
```
add "css/pigeon.css" to head tag in html page
add "css/bootstrap.css" to head tag in html page
add "js/jquery-3.1.1.min.js"(version not matters) to end of body tag
add "js/pigeon.js" to end of body tag to
```
### Usage
```
define a button with unique id
init plugin like this: 
$('select your button').pigeon({
    url:"your api address",
    //other params
});
```

### Options

| option | type | desc |
| --- | --- |--- |
|  url | string |  url of server api for sending each file seperatly
| maxFileCount | int | maximum number of files to upload, default is 10 |
| maxFileSize | int | maximum size of each file in MB, default is 5 |
| extentions | string | extentions of files like "image/*,application/pdf", default is "*" |
| checkedIcon | string | icon class used for check icon |
| errorIcon | string | icon class used for error icon |

### Some Points

* each file will be sent by key "file"
* its better to wrap button in a div with class "col-x(>3)"
* server reponse should be in json format with this props
* 1- IsSuccesssful
* 2- Message: message if there is an error

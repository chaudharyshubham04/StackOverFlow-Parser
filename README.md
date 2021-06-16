# StackOverFlow-Parser
Ever faced great difficulty in copying the error you’re stuck with, opening the browser, pasting it, and opening the right Stack Overflow Answer?  Worry Not, Here’s the solution! What we are going to do is to write a Python script, which automatically detects the error from code, search about it on Stack Overflow, and opens up the few tabs related to our error that were previously been answered also.


## Modules Used
The subprocess module is used to run new applications or programs through Python code by creating new processes. The subprocess module was created with the intention of replacing several methods available in the os module, which were not considered to be very efficient.
The requests module allows you to send HTTP requests using Python.
The webbrowser module allows us to launch the web browser.


### Approach: We will divide the script into three parts, i.e. we will create three functions as follows: 


#### * execute_return(cmd):
On the first function, we are going to write code to read and run python file, and store its output or error.


#### * mak_req(error):
This function will make an HTTP request using Stack Overflow API and the error we get from the 1st function and finally returns the JSON file.


#### * get_urls(json_dict):
This function takes the JSON from the 2nd function, and fetches and stores the URLs of those solutions which are marked as “answered” by StackOverflow. And then finally open up the tabs containing answers from StackOverflow on the browser.

Performance Testings

Its a non functional testing
It is to determine how application performs under particular load

There are many tools that helps us to do this. Jmeter is one of them

Why Jmeter ?
1) Open Source
2) 100% Pure Java and hence platform independent.
3) GUI is easy to use.

Installation
1) refer link for the download https://jmeter.apache.org/download_jmeter.cgi

How to Run Jmeter
1) navigate to bin folder of Jmeter --> C:\Software\apache-jmeter-5.6.2\apache-jmeter-5.6.2\bin
2) ApacheJMeter.jar --> run this file

Jmeter Elements
1) Test Plan - it's a jmeter script for running tests. It can be considered as a container for test.
2) Workbench - is was available in older versions of Jmeter (its like rough work section). We can ignore this now
3) Thread Group - it is a collection of threads. Each thread simulates a real user, making request to server. Each test plan must have atleast 1 thread group
4) Samplers - is a request in Jmeter, which needs to be made to the server. There are many samplers

Following are few important samplers
a) HTTP - this is to make HTTP request

5) Listeners - facilitates to view sampler's results in the form of table, graphs, simple text, etc. Listeners offer a means to collect, save, view the results of a test plan. There are different types of listeners
a) View Result Tree Listener - 

6) Config Elements - these are used to configure samplers
a) HTTP Header Manager - this is used to send additional headers to server. e.g. 'content-type'
b) HTTP Request Defaults - it isused to configure common things for multiple samples, such as base url, protocol, port numbers, etc. It is useful when we have multiple requests to the same server
c) User Defined Variables - Used to define user defined variables and can be used  using syntaxt : ${variableName}. variables can be defined at Test Plan level or Thread Group level.
d) CSV Data Set Config- it is used to fetch data line by line and store it in the variables separated by commas.
e) HTTP Cookie Manager - it is used to simulate browser activity by storing the cookie and sending the cookie back to server
f) HTTP Authorization Manager - it is used to handle browser authentication process ( basic authentication )

7) Assertions - these are used to apply validations on the response sent by server. there are following types of assertions:
a) Response Assertion - it is used to compare string patterns withing response. it can also be used to compare response code, response message
b) Duration Assertion - it is used to assert the response time from the server
c) Size Assertion - it is used to assert the response from server contains expected(>, <, =, !=) number of bytes
d) JSON Assertion - it can be used to check value of key from the json sent by server as response body
e) HTML Assertion - it is used to assert whether the page returned is following proper html format or not

8) Timers - Timers are used to add delay for a request. There ae following types of timers
a) Constant Timer - This is to add constant delay for a sampler(request)
b) Uniform Random Time - this is to add delay within range ( e.g. 100ms to 200ms) . Accepts 2 properties

9) PreProcessors - these are elements executed before samplers ( e.g. HTML Link Parser, BeanShellPreProcessor)

10) PostProcessor - These are elements executed after samplers ( e.g. Regular Expression Extractor )




Sequence of execution of differnt elements
1) Config Elements
-- 2) PreProcessor
---- 3) Timer
------ 4) Samplers
--------5) PostProcessor
-------- 6) Assertions
---------- 7) Listeners



UseCase

) With 5 users all users are hitting server at the same time
2) Users are visiting 3 pages
3) Before going to each page we need to have some waiting time
4) URL can change in future
5) Generate report











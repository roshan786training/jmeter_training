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


Sequence of execution of differnt elements
1) Config Elements
-- 2) Samplers
---- 3) Listeners


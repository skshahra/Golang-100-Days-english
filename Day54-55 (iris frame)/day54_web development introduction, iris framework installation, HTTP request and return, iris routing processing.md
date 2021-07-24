

# Introduction to web development, iris framework installation, HTTP request and return, Iris routing processing
**@author: Davie**  
**Copyright: Beijing Qianfeng Internet Technology Co., Ltd.**

## One Web project development introduction and actual project introduction
### 1.1 Introduction
In this series of courses, we will learn some related knowledge and usage of the web development framework Iris in the Golang language. Through this series of video courses, everyone can experience the development of a complete project from zero to one, and understand the actual project development process and the various modules involved in the project design in the course.

### 1.2 Introduction to Web Project Development
#### 1.2.1 Project Architecture  
The web project can be divided into two parts, the foreground and the background. The front desk is mainly the programs that we directly face the user in the browser or desktop applications, Android, iOS mobile applications, etc., directly accept the user's operation and use, we call it the front desk, also called the client; provide data for the front desk application The program running on the server for the deployment and function call is used to manipulate and process the data of the front-end application. We call it the background or the server. Similar to the above-mentioned client and server architecture, we usually call it the CS mode, C is the abbreviation of client, and S is the abbreviation of server.
#### 1.2.2 Development Process  
##### 1.2.2.1 Requirements determination 
In the requirement determination stage, the product manager is mainly responsible for determining the function and performance of the system. After confirming the specific requirements, the product manager will design the product function. This stage is usually called the product prototype design process. At this stage, the core goal is to determine development requirements and complete product prototype design.
##### 1.2.2.2 Analysis and Design  
After the requirements are determined, the next step is to analyze and design. In this stage, it is divided into several small stages, namely: architecture analysis and design, business logic analysis, business logic design, and interface design.  
	Architecture analysis and design: logical architecture, physical architecture (server configuration, database configuration), technology selection, etc. 
	Business logic analysis: system users, purpose of use, operation steps, user experience and feedback, etc.  
	Business logic design: detailed database design, object relational field mapping, etc.   
	Interface design: UI style, user experience, etc.
##### 1.2.2.3 Development environment setup
When the requirements and design phases are determined, the development phase is officially entered. The first is the establishment of the development environment, which includes two kinds of hardware environment and software environment. The hardware environment refers to the development machines, servers and other hardware facilities. The software environment includes software support such as development tools, project management platform, and software support. The establishment of the development environment generally only needs to be carried out when the project has just started and when the project is undergoing major structural adjustments. Under normal circumstances and daily iterative development, this step can be omitted and the existing development environment can be used directly.
##### 1.2.2.4 Development and Testing
In the actual project development cycle, the code development cycle is often shorter. At the same time, after the code function development is completed, the system function needs to be tested. At this time, the project testers conduct professional white box testing, black box testing, performance testing, stress testing and other comprehensive and multi-angle system testing. The development and testing at this stage are carried out alternately. In the actual development process, multiple rounds will be repeated to ensure the correctness of the functions developed by the developers and the stability of the system.  
When the system development and testing phase is over, the code will be sealed for final testing. If the final test passes, it will be deployed and launched.
##### 1.2.2.5 Document editing
In the process of system design, project development and testing, we must follow a set of standardized development steps that are suitable for team use and executable acceptable. In the process of project development, we need to compile and properly save documentary content such as project development, operation instructions, project structure instructions, etc., so that in the subsequent project maintenance and docking process, relevant personnel can correctly and quickly understand and be familiar with the project .  
  
### 1.3 Introduction to the actual combat project function
In this series of courses, we will take you to the actual development of a back-end management platform project to help you learn the relevant usage and project development process of the Iris framework.
#### 1.3.1 Project effect
First, let's take a look at the effect of the overall operation of the project:  
![Background management platform login interface](./img/iris background management system.png)
![Background management platform main interface](./img/iris background main interface.png)

#### 1.2.2 Project Structure
* Front end: vue framework
* Backend: Go language Iris framework + mysql database, redis cache database
* Interface documentation tool:  
	Xiaoyaoji: [http://www.xiaoyaoji.cn/doc/yvnmPtdKK](http://www.xiaoyaoji.cn/doc/yvnmPtdKK)
* Interface debugging tool: Postman

#### 1.2.3 Project development cycle
A week

## Two Iris framework
### 2.1 Introduction to Golang
Go language is a brand new programming language launched by Google, which can reduce the complexity of the code without losing the performance of the application. Rob Pike, Google's chief software engineer, said: We developed Go because of the frustrating difficulty of software development over the past 10 years.  
Rob Pike, a senior software engineer at Google, said, “Go allows me to experience development efficiency that I have never had before.” Pike said that like C++ or C today, Go is a system language. He explained, "It can be used for rapid development, and it is still a real compiled language. The reason why we open source it now is because we think it is already very useful and powerful."  
Some features of Golang language:
* With modern programming language features, such as garbage collection, it helps programmers deal with trivial and important memory management issues. Go is also very fast, almost as fast as C or C++ programs, and can quickly make programs.
* The software is designed for building server software (such as Google's Gmail). Google believes that Go can also be applied to other areas, including executing software in the browser, replacing the role of JavaScript.  
* Go can also solve a major challenge today: multi-core processors. Normal computer programs are usually executed sequentially, one job at a time, but multi-core processors are more suitable for processing many jobs in parallel.
Compared with other languages, the rapid development of Golang is inseparable from the unique characteristics of the language:  
* Simple, fast and safe
* Parallel, interesting and open source
* Memory management, array security, fast compilation

### 2.2 Introduction to Iris
Iris is a framework for developing web applications in the Go language. The framework supports writing once and running with minimal machine power anywhere, such as Android, ios, Linux, and Windows. The framework only needs an executable service to run on the platform.  
The Iris framework is familiar to developers with its simple and powerful API. In addition to providing developers with a very simple access method, iris also supports MVC. In addition, it is easy to build microservices with iris.  
On the official website of the iris framework, it is known as the fastest Go back-end development framework. On the Iris website document, some of the characteristics and characteristics of the framework are listed as follows:
1) Focus on high performance   
2) Robust static routing support and wildcard subdomain name support  
3) The view system supports more than 5 templates  
4) Highly scalable Websocket API supporting customized events  
5) Sessions with GC, memory & redis support  
6) Convenient middleware and plug-ins  
7) Complete REST API  
8) Can customize HTTP errors  
9) Automatically load after source code changes  
There are many other features, you can refer to the official Iris documentation. Among the many frameworks developed by GoWeb, the performance of each dimension is compared as follows:
 ![Iris framework performance comparison with other languages](./img/Go language performance comparison.png)
 ![GoWeb framework development efficiency comparison](./img/Go language web framework comparison.png)
 
### 2.3 Iris framework learning channel
When learning the Iris framework process, we need to have the corresponding supporting materials to be able to complete our learning. The following are the materials that may be used in the process of learning the Iris framework.  
#### 2.3.1 Official website
Iris official website: [https://iris-go.com/](https://iris-go.com/)  
#### 2.3.2 Framework source code
Iris framework source code address: [https://github.com/kataras/iris](https://github.com/kataras/iris)  
#### 2.3.3 Framework Learning Document
Iris framework Chinese learning document: [https://studyiris.com/doc/](https://studyiris.com/doc/) 
Of course, there are other related materials, such as xorm framework, etc., which we will explain and explain after learning in the course documents.  

### 2.4 Iris frame installation
#### 2.4.1 Go version restrictions
**Environmental requirements: **The iris framework requires golang version at least 1.8. You can check the go environment version of your machine by opening the terminal and executing: go version command.
#### 2.4.2 Command installation
Installing the Iris framework is very simple, just use the go command to install third-party code globally. The command to install the Iris framework is as follows:    
```  
go get -u github.com/kataras/iris
```
Execute the above installation command in the local terminal and wait for the command to execute successfully, which means that the Iris source code download and installation is complete. After the Iris framework is installed, the package name corresponding to the iris framework can be found in the src/github.com/ directory in the GoPath environment directory of the local machine, as shown in the following figure:  
![Iris framework source code installation picture](./img/Iris source code structure.png)
As shown in the figure, the directory where kataras/iris is located is the source code of the iris framework. As shown in the figure above, the installation is successful.  

### 2.5 Source code case
After the iris source code is installed, the iris framework provides developers with practical cases for their own learning. The cases provided by iris are in the _example directory in the iris framework directory, and you can refer to them when you study.
Next, we can start to learn about iris and proceed with code development.

### 2.6 Iris construct service instance  
After installing the source code of Iris, we started to write the simplest Iris service. In Iris, building and running a service instance requires two steps:  

* 1. An application service object app can be instantiated through the iris.New() method  
* 2. Use the Run method to open the port monitoring service and run the service instance

The following is the simplest service case Demo
```go
package main
import "github.com/kataras/iris"
func main() {
	//1. Create app structure object
	app := iris.New()
	//2. Port monitoring
	app.Run(iris.Addr(":7999"), iris.WithoutServerError(iris.ErrServerClosed))
	////application.Run(iris.Addr(":8080"))//The first
	//application.Run(iris.Addr(":8080"), iris.WithoutServerError(iris.ErrServerClosed)) //The second
}
```

## Three Get, Post, Put and other requests and data return format
### 3.1 Classification of data request methods
All requests used in the project follow the HTTP protocol standard, and the HTTP protocol has been developed in two versions, 1.0 and 1.1.
#### 3.1.1 HTTP1.0 
HTTP1.0 defines three request methods: GET, POST and HEAD methods.
#### 3.1.2 HTTP1.1
HTTP1.1 adds five new request methods: OPTIONS, PUT, DELETE, TRACE and CONNECT methods.

Therefore, we can say that the HTTP protocol defines a total of eight methods for different operations on Request-URI network resources. These operations are specifically: GET, POST, PUT, DELETE, HEAD, OPTIONS, TRACE, CONNECT, etc. Operation method.

### 3.2 Request processing method of Iris framework
#### 3.2.1 Default request processing
The service instance app in the Iris framework contains multiple methods to support the direct processing of the above-mentioned HTTP request types, which are directly defined as get methods, post methods, put methods, etc. The methods included in the app to automatically process routing requests are the same as The classification of http request types is the same.
```go
app := iris.New()
//url: http://localhost:8000/getRequest
//type: GET request
app.Get("/getRequest", func(context context.Context) {
		path := context.Path()
		app.Logger().Info(path)
})
```
#### 3.2.2 Handle custom processing
In addition to the automatic processing of various types of requests in 1 above, the framework also supports the use of the general Handle method to customize and write your own request processing types and corresponding methods.
```go
//url: http://localhost:/user/info
//type: POST request
app.Handle("POST", "/user/info", func(context context.Context) {
		context.WriteString(" User Info is Post Request, Deal is in handle func ")
})
//Start port monitoring service
app.Run(iris.Addr(":8000"))
```

#### 3.2.3 GET request
Initiate a request for specific network resource data. GET request can carry request data, what will the request data carry? Split the URL and transfer data, and connect the parameters with &, such as http://localhost:3000?name=davie&pwd=123.  
The following is an http get type request:  
```
http://localhost:8000/userpath
```
The routing processing method of the server is as follows:  
```go
//url: http://localhost:8000/userpath
//type: GET request, processed by GET method
app.Get("/userpath", func(context context.Context) {
		//Get Path
		path := context.Path()
		//Log output
		app.Logger().Info(path)
		//Write return data: string type
		context.WriteString("Request path:" + path)
})
```
The above is to use the encapsulated default app.Get method to process the request, and use the Handle method to process the request, as shown below:  
```go
//url: http://localhost:8000/hello
//type: GET request, the first parameter of the Handle method is GET, indicating that it is a GET request method
app.Handle("GET", "/hello", func(context context.Context) {
		context.HTML("
 Hello world. 
")
})
```

#### 3.2.4 POST request
POST requests put the request data in the request body when making a request, and there is no limit to the size of the request data. During the development process, we use the postman tool to debug POST requests.  
An example of a POST request is shown below:  
```
http://localhost:8000/postLogin
```
The routing processing method of the server is as follows:
```go
//type: POST request
//Carry data: request data named by name and pwd
app.Post("/postLogin", func(context context.Context) {
		//Get request path
		path := context.Path()
		//Log
		app.Logger().Info(path)
		//Get request data field
		name := context.PostValue("name")
		pwd, err := context.PostValueInt("pwd")
		if err != nil {
			panic(err.Error())
		}
		app.Logger().Info(name, "", pwd)
		//return
		context.HTML(name)
})
```
The above is to use the default route request method Post method for processing, at the same time, you can also use the Handle method for processing, as shown in the following figure: 
```go
//url: http://localhost:8000/user/info
//type: POST request, the first parameter of the Handle method is POST, indicating that it is a Post request
app.Handle("POST", "/user/info", func(context context.Context) {
		context.WriteString(" User Info is Post Request, Deal is in handle func ")
})
```

#### 3.2.5 PUT, DELETE, OPTIONS, HEAD and other types of requests  
In addition to the two most common request methods of GET and POST, there are other types of requests such as PUT, DELETE, OPTIONS, and HEAD. For other types of requests, just like GET and POST requests, they can be done in two ways. handle:  
* 1. The processing request method provided by the iris framework to automatically identify the request type, such as put method, head method, options method, delete method, etc.
* 2. Use the general Handle method to process the routing request. The developer himself chooses the specific request type, the corresponding url and the func to be processed.  

The following is the request processing of put and delete:   
PUT request
```go
//type: PUT type request
app.Put("/putinfo", func(context context.Context) {
		path := context.Path()
		app.Logger().Info("Request url:", path)
})
```

DELETE request
```go
//type: DELETE type request  
app.Delete("/deleteuser", func(context context.Context) {
		path := context.Path()
		app.Logger().Info("Delete request url:", path)
})
```

### 3.3 Return of the requested data format  
In this lesson, we have learned how to process different types of requests and how to obtain the data carried in the request. When the request is received in the background, the request will be processed, and the data will be returned to the requesting party after processing. Client. Next, let's take a look at how to return the data and what forms it has.
During request processing, the processing method func has a parameter context. Context is a context environment variable used to process requests, used to process http requests and related data returns. The iris framework supports the return of multiple data formats. Here we learn to return data in string, json, xml and html formats.
#### 3.3.1 Return string type data   
```
context.WriteString("hello world")
``` 
#### 3.3.2 Return data in json format  
```
context.JSON(iris.Map{"message": "hello word", "requestCode": 200})
```
#### 3.3.3 Return data in xml format  
```
context.XML(Person{Name: "Davie", Age: 18})
```
#### 3.3.4 Return html format data  
```
context.HTML("
 Davie, 12 
")
```
Through the content of this lesson, we have learned the different types of data requests in the iris framework and the different data formats returned.

## Four routing function processing methods
### 4.1 Context concept
Context is a routing context object in the iris framework. The source code path in the iris framework is defined as: {$goPath}\github.com\kataras\iris\context\context.go. The following is the declaration and definition of Context:
```
package context
type Context interface {
	BeginRequest(http.ResponseWriter, *http.Request)
	EndRequest()
	ResponseWriter() ResponseWriter
	ResetResponseWriter(ResponseWriter)
	Request() *http.Request
	SetCurrentRouteName(currentRouteName string)
	GetCurrentRoute() RouteReadOnly
	Do(Handlers)
	AddHandler(...Handler)
	SetHandlers(Handlers)
	Handlers() Handlers
	HandlerIndex(n int) (currentIndex int)
	Proceed(Handler) bool
	HandlerName() string
	Next()
	NextOr(handlers ...Handler) bool
	NextOrNotFound() bool
	NextHandler() Handler
	Skip()
	StopExecution()
	IsStopped() bool
	Params() *RequestParams
	Values() *memstore.Store
	Translate(format string, args ...interface{}) string
	Method() string
	Path() string
	RequestPath(escape bool) string
	Host() string
	Subdomain() (subdomain string)
	IsWWW() bool
	RemoteAddr() string
	GetHeader(name string) string
	IsAjax() bool
	IsMobile() bool
	Header(name string, value string)
	ContentType(cType string)
	GetContentType() string
	GetContentLength() int64
	StatusCode(statusCode int)
	GetStatusCode() int
	Redirect(urlToRedirect string, statusHeader ...int)
	URLParamExists(name string) bool
	URLParamDefault(name string, def string) string
	URLParam(name string) string
	URLParamTrim(name string) string
	URLParamEscape(name string) string
	View(filename string, optionalViewModel ...interface{}) error
	Text(text string) (int, error)
	HTML(htmlContents string) (int, error)
	JSON(v interface{}, options ...JSON) (int, error)
	JSONP(v interface{}, options ...JSONP) (int, error)
	XML(v interface{}, options ...XML) (int, error)
	Markdown(markdownB []byte, options ...Markdown) (int, error)
	......
```  
In the Context interface definition, we can find that it contains many operations for processing requests and returning data. In the iris framework, developers are provided with a ContextPool, which is a management pool that stores the context variable Context. There are multiple context instances in the variable pool that can be reused. Every time there is a new request, a new context variable instance will be obtained to process the request routing. In the actual case study, we will show you the relevant usage of Context.

### 4.2 Regular expression routing
When processing http requests, the Iris framework supports regular expressions in the request url.  
The specific rules of regular expressions are:  
* 1. Use {} to wrap the increased regular expression, and a format similar to {} appears in the URL, which is recognized as a regular expression  
* 2. Support the naming of variables of self-defining regular expressions, and the variable names are represented by letters. For example: {name}  
* 3. Support the data type restriction of custom regular expression variables. The variable name and the corresponding data type are separated by ":". For example: {name:string} means the increasing regular expression is name, and the type is limited to string type
* 4. Get the variable of the increasing regular expression in the corresponding request url through the Get() and GetXxx() series methods of context.Params()
* 5. The data types of variables supported by regular expressions include: string, int, uint, bool, etc.

The following is an example of a regular expression request:  

```go
app.Get("/api/users/{isLogin:bool}", func(context context.Context) {
	isLogin, err := context.Params().GetBool("isLogin")
	if err != nil {
		context.StatusCode(iris.StatusNonAuthoritativeInfo)
		return
	}
	if isLogin {
		context.WriteString("Logged in")
	} else {
		context.WriteString("not logged in")
	}
})
```

  



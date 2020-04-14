
### REST API Application using  PHP, Slim and MySQL

## HTTP Methods
The application supports the following HTTP Metods: (GET, POST, PUT and DELETE).
GET	To fetch a resource
POST	To create a new resource
PUT	To update existing resource
DELETE	 To delete a resource

## HTTP Status Code
The Application supports the following HTTP codes:
200	OK
201	Created
304	Not Modified
400	Bad Request
401	Unauthorized
403	Forbidden
404	Not Found
422	Unprocessable Entity
500	Internal Server Error 

# Slim PHP Framework
Instead of starting to  develop a fresh REST framework from scratch, it is better to go with a already proven framework. For this application, I decided to go with Slim PHP Framework because of the following reasons: 
It is very light weight and clean.
Supports all HTTP methods GET, POST, PUT and DELETE which are necessary for a REST API.
More importantly it provides a middle layer architecture which will be useful to filter the requests. In this application, it has been used for verifying the API Key.
Slim Download Link:  https://github.com/codeguy/Slim

# Install  XAMP Server

XAMP lets you install Apache, PHP and MySQL with a single installer which reduces burden of installing & configuring them separately. Alternatively you can use WAMP, LAMP (on Linux) and MAMP (on MAC). XAMP also provides you phpmyadmin to easily interact with MySQL database.
Download and Install XAMP. Choose the correct version which suits your operating system (32bit or 64bit).
Open http://localhost/ and http://localhost/phpmyadmin/ to verify XAMP is installed successfully or not.

# Install Chrome Advanced REST client extension for Testing
Chrome Advanced REST client extension provides an easy way to test the REST API. It provides lot of options like adding request headers, adding request parameters, changing HTTP method while hitting a url. Once you installed it you can find it in chrome Apps or an icon at the top right corner.

Alternately,you can also use Postman: https://www.postman.com/downloads/ for testing. 

# Testing the API
Following is the list of URL needed to test using Chrome Advanced REST client extension and Postman with possible combinations of inputs.

You can notice that same url endpoint is used for multiple api calls, but the difference is the type of HTTP method we use to hit the url. Suppose if we hit /tasks with POST method, a newer task will be created. As well if we hit /tasks with GET method, all the tasks will be listed.

URL	Method	Parameters	Description
http://localhost/task_manager/v1/register	POST	name, email, password	User registration
http://localhost/task_manager/v1/login	POST	email, password	User login
http://localhost/task_manager/v1/tasks	POST	task	To create new task
http://localhost/task_manager/v1/tasks	GET		Fetching all tasks
http://localhost/task_manager/v1/tasks/:id	GET		Fetching single task
http://localhost/task_manager/v1/tasks/:id	PUT		Updating single task
http://localhost/task_manager/v1/tasks/:id	DELETE	task, status	Deleting single task


# Creating MySQL Database

For this Application, I have created three tables: users, tasks and user_tasks.
users – All user related data will be stored here. A row will be inserted when a new user register in the app.
tasks – All user tasks data will be stored in this table
user_tasks – Table used to store the relation between user and his tasks. Basically it will store users id and task id.

Download and Import the database. 





1-> Essentially we are going to sign into Clerk on our Frontend
2->  clerk is going to authorize the user and it's going to issue us an authentication token. 
3-> that token we can then use to send to the backend, and our backend can go and ask Clerk says is this token valid, if it says yes, means this user has the permissions to access our backend service.

We need to wrap the application in this clerk provider



corsmiddleware-> CORS middleware is a middleware that allows you to configure CORS (Cross-Origin Resource Sharing) for your web application . our frontend can send request to our backend and our backend can send request to our frontend.

uvicorn-> a webserver that allow us to serve our fast api application
(so we running the application that we imported from this app file on the local computer on localhost port 8000)



clerk with authentication us on the frontend and it's going
to issue something called as JWT token which is a json web token, Now this token can then be sent to the backend
and on the backend, we can check that this token is valid or not. 

and we don't have to wait for the clerk respone  we can do this network list  is because we have JWT_key and secret key is able to look at thses clerk tokens and see if they are valid or not








-----------
Yes, SQLite is a serverless database. This means it doesn't require a separate server process to opertate.
. Instead, it's a library that applications can directly link to, reading and writing data to disk files. Because it's serverless, it's often favored for embedded systems, mobile applications, and situations where a lightweight, zero-configuration database is needed


--------------
SQLAlchemy is primarily used as a Python SQL toolkit and Object Relational Mapper (ORM) for interacting with databases. It allows developers to work with databases using Python objects, providing a Pythonic way to handle database connections, query construction, and data management
Database Abstraction:
SQLAlchemy provides a layer of abstraction that allows you to interact with various databases (like PostgreSQL, MySQL, SQLite, etc.) using a consistent interface, without needing to write specific SQL code for each database

Object-Relational Mapping (ORM):
The ORM component of SQLAlchemy maps Python classes to database tables and automatically translates Python operations into SQL queries. This allows developers to work with objects and their relationships in Python, rather than writing raw SQL

SQLAlchemy allows you to build SQL queries using Python code, making it easier to create complex queries and manage data manipulation








we are going to authenticate this request(from frontend)
by getting a particular token, we can then decode that token and in that token it will contain the user id, the email and the user name which is under the field sub(check utils.py on backend).




Database------
ORM-> allow us to write python classes that represent sql tables.
engine -> what database we are going to use
declarative_base()-> this is going to be the base class for all our tables, which is going to be the parent class for all our tables.

yield in python-> generator function
db.py-> helper function for interacting with this database

----------------
routes-> things we are going to call, essentially the slash endpoints on our api

APIRouter-> allow use to make our code more module and have differnt routes in differnt files

Pydantic Schema is something that fastapi can use to validate that the data being sent to the endpoint is correct.
------------------------
**challenge_data(is a dictionary) ->these asteriks means that we are going to unpack this dictionary. and passes all of the jeys and values as arguments to the function.
------------
clerk webhook=>why-> when a new user was created,their quota wasn't being set. that's because when a new user is made, we should just automatically set the quota for them.
so that  any time an event happens in clerk,we want to subscrie to, it  automatically push this event to our webhook endpoint(our backend).

---------------
the signing secret - we take it to the backend because we need to set up an endpoint that clerk can send these events to so that we can handle them
------
ngrok api gateway -> to test the webhook on our local computer, we need to use ngrok to expose our local server to the internet.


----
Context Manager in python-> even if an error occurs inside of this  inside of this indented block , the exit operation will still be called so we safely know that we can deal with the file and automatically close it whether an operation works or not.



like in the case of a lock,
the enter operation will be retrieving the lock or waiting for it to be opened 
and the exit operation will release the lock and let another thread use it.
from contextlib import suppress

with suppress(FileNotFoundError):
    open("non_existent_file.txt")
# No exception is raised, program continues smoothly
# ----------------------------------------------
import tempfile
with tempfile.TemporaryFile(mode='w+t') as tmp:
    tmp.write("Temporary data")
    tmp.seek(0)  # Go back to start of file to read
    data = tmp.read()
    print(data)
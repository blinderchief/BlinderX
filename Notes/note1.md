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
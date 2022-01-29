# python-easyblog based on Django blog tutorial
See the tutorial series at this link: [dontrepeatyourself.org](https://dontrepeatyourself.org)

## Deployment method

### Heroku Git
 
[GitHub][Connected][App connected to GitHub][Deploy a GitHub branch][This will deploy the current state of the branch you specify below][Choose a branch to deploy]

### Install the Heroku CLI
Download and install the Heroku CLI.

If you haven't already, log in to your Heroku account and follow the prompts to create a new SSH public key.
~~~
$ heroku login
~~~
Clone the repository
Use Git to clone python-easyblog's source code to your local machine.
~~~
$ heroku git:clone -a python-easyblog$ cd python-easyblog
~~~
Deploy your changes
Make some changes to the code you just cloned and deploy them to Heroku using Git.
~~~
$ git add .
$ git commit -am "make it better"
$ git push heroku master
~~~

### Install the Heroku CLI
Download and install the Heroku CLI.

If you haven't already, log in to your Heroku account and follow the prompts to create a new SSH public key.
~~~
$ heroku login
~~~
Log in to Container Registry
You must have Docker set up locally to continue. You should see output when you run this command.
~~~
$ docker ps
~~~
Now you can sign into Container Registry.
~~~
$ heroku container:login
~~~
Push your Docker-based app
Build the Dockerfile in the current directory and push the Docker image.
~~~
$ heroku container:push web
~~~
Deploy the changes
Release the newly pushed images to deploy your app.
~~~
$ heroku container:release web
~~~

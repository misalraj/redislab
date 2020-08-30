# redislab
Redis labs materials

#Lab Setup 

Lab setup

1. Download and install Redis. The minimum version is 5.0.3 for this course.
    sudo apt-get install redis-server

2. Confirm you have a viable Python environment

1. Confirm Python 3.6.5 or above

$ python --version
Python 3.6.5
2. Confirm pip 9.01 or above

$ pip3 --version
pip 19.0.1 from /usr/lib/python3.6/site-packages/pip (python 3.6)
3. Required python packages installed

$ pip3 install --upgrade --no-cache-dir redis==3.0.1 Faker

clone the repo

5. Redis Host

The sample code will try to connect to Redis on localhost on port 6379. If Redis is running on a different Host or Port, then you need to set the following environment variables:

REDIS_HOST: The IP address or hostname of your Redis server, eg. test06.acme.com

REDIS_PORT: The port number that the Redis server is listening on, e.g. 12405

6. Validate your PYTHONPATH

$ python helloworld.py
None 
If you receive errors failing to import packages, then confirm your PYTHONPATH environment variable (or equivalent) includes the path to the director where you unzipped the source code from step 4.

7. Load the sample data

The exercises and homework rely on a sample set of data. This data can be loaded as follows

$ python utils/dumpload.py load ru101/data/ru101.json 
total keys loaded: 14328
When you run helloworld.py again, this time it should print "world".

$ python helloworld.py
world
You can also confirm the number of key present in the redis-cli as follows

> dbsize
(integer) 14328
Option 3 - Run the Lab in your local Docker environment
If you have access to a Docker environment, a Docker image has been created that encapsulates the IDE, Redis Server, source code and sample data. Follow these instructions to use the image.

1. Run the Docker container

$ docker run --rm --name redis-lab -p:8888:8888 redisuniversity/ru101-lab
2. Point your browser to

localhost:8888/entry.html

Windows 10
A number of students have had success running the course of Windows 10 (using the April 2018 release). This is not something we have tried ourselves. Please note that there is no active port of Redis for Windows, and software you may find is very out of dates (e.g. 3.2.1).

Students have been successful by using the Windows subsystem for Linux, and install the Linux version of Redis. See the following articles

https://docs.microsoft.com/en-us/windows/wsl/install-win10 

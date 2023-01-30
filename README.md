# Name: Sushma Pamidi
# Link to Repo: https://github.com/pamidisushma02/streaming-04-multiple-consumers

# streaming-04-multiple-consumers

> Use RabbitMQ to distribute tasks to multiple workers

One process will create task messages. Multiple worker processes will share the work. 


## Before You Begin

1. Fork this starter repo into your GitHub.
### Done

2. Clone your repo down to your machine.
### Done

3. View / Command Palette - then Python: Select Interpreter
### Done

4. Select your conda environment. 
### Done

## Read

1. Read the [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)
   Read this tutorial
   ### Done

2. Read the code and comments in this repo.
   ### Done

## RabbitMQ Admin 

RabbitMQ comes with an admin panel. When you run the task emitter, reply y to open it. 

(Python makes it easy to open a web page - see the code to learn how.)

## Execute the Producer

1. Run emitter_of_tasks.py (say y to monitor RabbitMQ queues)

Explore the RabbitMQ website.

## Execute a Consumer / Worker

1. Run listening_worker.py

Will it terminate on its own? How do you know? 

### Response: No it does not terminate on its own. I tried to second another message by modifying the message in the emitter_of_tasks.py. When I tried to run the process it did not. This is because the consumer i.e. listening_worker.py did not terminate
### We can not execute any other command on the terminal. We can use ctrl + C to terminate the process and then run any other command


## Ready for Work

1. Use your emitter_of_tasks to produce more task messages.

### Response: I used multiple terminals (4 Producer terminals and sent multiple messages). Please refer to the below screen shots

## Start Another Listening Worker 

1. Use your listening_worker.py script to launch a second worker. 

### Response: I used 2 listening workers (2 consumers)


Follow the tutorial. 
Add multiple tasks (e.g. First message, Second message, etc.) - 
### Response: Done


How are tasks distributed? - 

### Response: In round-robin. I had observed that both the consumer terminals received alternate messages. First one received First tast, Third task, Fifth etc. Second terminal received Second task, Fourth task


Monitor the windows with at least two workers. 

### Response: Done


Which worker gets which tasks? 

### Response: As mentioned above, I had observed that both the consumer terminals received alternate messages. First one received First tast, Third task, Fifth etc. Second terminal received Second task, Fourth task


## Reference

- [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)


## Screenshot

# Below Screen shots are using Version 1 & 2 code base 
## (for the more interesting screenshots from Version 3, please scroll down below)

## Producer Terminal 1
![Producer Terminal 1]( https://github.com/pamidisushma02/streaming-04-multiple-consumers/blob/main/Producer_Terminal%201.PNG "Terminal 1")

## Producer Terminal 2
![Producer Terminal 2](https://github.com/pamidisushma02/streaming-04-multiple-consumers/blob/main/Producer_Terminal%202.PNG "Terminal 2")

## Producer Terminal 3
![Producer Terminal 3](https://github.com/pamidisushma02/streaming-04-multiple-consumers/blob/main/Producer_Terminal%203.PNG "Terminal 3")

## Producer Terminal 4
![Producer Terminal 4](https://github.com/pamidisushma02/streaming-04-multiple-consumers/blob/main/Producer_Terminal%204.PNG "Terminal 4")

## Consumer Terminal 1
![Consumer Terminal 1](https://github.com/pamidisushma02/streaming-04-multiple-consumers/blob/main/Consumer_Terminal%201.PNG "Terminal 5")

## Consumer Terminal 2
![Consumer Terminal 2](https://github.com/pamidisushma02/streaming-04-multiple-consumers/blob/main/Consumer_Terminal%202.PNG "Terminal 6")


# Below Screen shots are using Version 3. Additional tasks are added to the tasks.csv file
## Version 3 Producer Terminal (We are just using one terminal and this one reads all the tasks from the tasks.csv file)
![Producer Terminal]( https://github.com/pamidisushma02/streaming-04-multiple-consumers/blob/main/Version%203_Producer_Terminal_using%20tasks.PNG "Terminal 1")

## Version 3 Consumer Terminal 1
![Consumer Terminal 1](https://github.com/pamidisushma02/streaming-04-multiple-consumers/blob/main/Version%203_Consumer_Terminal%201.PNG "Terminal 2")

## Version 3 Consumer Terminal 2
![Consumer Terminal 2](https://github.com/pamidisushma02/streaming-04-multiple-consumers/blob/main/Version%203_Consumer_Terminal%202.PNG "Terminal 3")

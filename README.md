# rabitmq


How to Install Erlang on Ubuntu 18.04 & 16.04 LTS
Written by Rahul, Updated on March 12, 2020

 
Erlang is a programming language used to build massively scalable soft real-time systems with requirements on high availability. Erlang runtime system has built-in support for concurrency, distribution and fault tolerance. This tutorial will help you to install Erlang on Ubuntu 18.04 and 16.04 using PPA.

Step 1 – Adding Repository

First, use the following commands to add erlang apt repository on your system. You can simply download erlang repository package from its official website and install on your system.

wget https://packages.erlang-solutions.com/erlang-solutions_1.0_all.deb
sudo dpkg -i erlang-solutions_1.0_all.deb
Step 2 – Install Erlang on Ubuntu

Now, you can install an erlang package on your system using the following command. This will install all of its dependencies as well.

sudo apt-get update
sudo apt-get install erlang
Alternatively, you can do the complete erlang installation. It includes the Erlang/OTP platform and all of its applications.

sudo apt-get update
sudo apt-get install esl-erlang
Step 3 – Erlang Hello World Program

Let’s start with hello world program on erlang. First create file helloworld.erl with following content.

vi helloworld.erl
add the following contnet.

% hello world program
-module(helloworld).
-export([start/0]).

start() ->
io:fwrite("Hello World!\n").
Now compile the hello world program using below command.

erlc helloworld.erl
The above command will create a file helloworld.beam in the current directory. You can run your program now.

erl -noshell -s helloworld start -s init stop

Hello World!

# sync package metadata
sudo apt-get update
# install dependencies manually
sudo apt-get -y install socat logrotate init-system-helpers adduser

# download the package
sudo apt-get -y install wget
wget https://github.com/rabbitmq/rabbitmq-server/releases/download/v3.8.5/rabbitmq-server_3.8.5-1_all.deb

# install the package with dpkg
sudo dpkg -i rabbitmq-server_3.8.5-1_all.deb

rm rabbitmq-server_3.8.5-1_all.deb


echo 'deb https://packages.erlang-solutions.com/ubuntu xenial contrib' | sudo tee -a /etc/apt/sources.list

wget https://packages.erlang-solutions.com/ubuntu/erlang_solutions.asc

sudo apt-key add erlang_solutions.asc

apt update && apt install esl-erlang

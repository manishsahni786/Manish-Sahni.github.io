# Introduction
Leon is an open-source personal assistant who can live on your server.He does stuff when you ask him to.

You can talk to him and he can talk to you. You can also text him and he can also text you. If you want to, Leon can communicate with you by being offline to protect your privacy.

## Why?

- If you are a developer (or not), you may want to build many things that could help in your daily life. Instead of building a dedicated project for each of those ideas, Leon can help you with his Skills structure.

- With this generic structure, everyone can create their own skills and share them with others. Therefore there is only one core (to rule them all).

- Leon uses AI concepts, which is cool.

- Privacy matters, you can configure Leon to talk with him offline. You can already text with him without any third party services.

- Open source is great.
## What is this repository for?
Link for Repo: https://github.com/leon-ai/leon

This repository contains the following nodes of Leon:

- The server
- Skills
- The web app
- The hotword node
- The TCP server (for inter-process communication - between Leon and third-party processes such as spaCy)
- The Python bridge (the connector between Python core and skills)
## Getting Started
---
## Prerequisites
- Node.js >= 16
- npm >= 8
- Supported OSes: Linux, macOS and Windows

To install these prerequisites, you can follow the How To section of the documentation.

Link is: https://docs.getleon.ai/how-to/

## Installation

``` bash 
# Install the Leon CLI
npm install --global @leon-ai/cli

# Install Leon (stable branch)
leon create birth
# OR install from the develop branch: leon create birth --develop
```
## Usage
``` bash
# Check the setup went well
leon check

# Run
leon start

# Go to http://localhost:1337
# Hooray! Leon is running
```
```bash
Docker Installation
# Install Leon
leon create birth --docker

# Run
leon start

# Go to http://localhost:1337
# Hooray! Leon is running
```
## 📚 Documentation
---
For full documentation, visit docs.getleon.ai.

## 📺 Video
---
Watch a demo.

Link :https://www.youtube.com/watch?v=p7GRGiicO1c

## 🧭 Roadmap
---
To know what is going on, follow roadmap.getleon.ai.

❤️ Contributing
---
If you have an idea for improving Leon, do not hesitate.

Leon needs open source to live, the more skills he has, the more skillful he becomes.

## 📖 The Story Behind Leon
---
You'll find a write-up on this blog post.

Link :https://blog.getleon.ai/the-story-behind-leon/

----
## Problems and Errors faces during installation of Leon.

1. After running the  command leon create birth
 I faced any error saying:

manny@manny-GF63-Thin-10SC:~/Desktop$ sudo leon create birth
- ✔ Installing packages
- ✔ Installing Python
- ✔ Downloading Leon source code
- ✖ Installing npm dependencies

Error: Could not install the npm dependencies
For further information, look at the log file located at
/root/.config/@leon-ai/cli/log-errors.txt
Trying to find a solution for this error.

2. And after that runing the same command again on     terminal there is an another error shown.

manny@manny-GF63-Thin-10SC:~$ leon create birth

Error: /home/manny/.leon already exists, please provide another path.

I found the solution to this error Error: /home/manny/.leon already
exists, please provide another path
by removing the directory .leon from my system by using command = rm
-rf .leon and now leon create
birth command is executing after that i will give further report.

Solve both errors by runing following command:

``` bash
manny@manny-GF63-Thin-10SC:~$ rm -rf /.leon
```
After that i run the following commands.
``` bash
manny@manny-GF63-Thin-10SC:~$ leon create birth
```
- ✔ Downloading Leon source code
- ✔ Installing npm dependencies
- ✔ Building Leon core

Success: Leon is born! 🎉
You can start your leon instance:
exec $SHELL
leon start

Finally I started Leon on my linux system at the local host
server at  http://localhost:1337 by running command
leon start in the terminal.
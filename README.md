# SockDrop
A client-server pipeline implemented with python socket programming to serve basic file sharing functionality.

## Description
- There are three parts of the project	- ![1_before_thread](/1_before_thread) , in which one box can run server and other client. Client can ask for any service via command line interface and it is served by the server on the other side.
	

## Features
- There are several command line commands implemented. See ![here](/problem_statement.pdf) for full description of commands.
	- `index longlist` : to list files residing on the other side, along with their details
	- `index shortlist` : to list files residing on the other side, between two specific timestamps
	- `index regex` : to list files residing on the other side, matching some patterns in their names
	- `hash verify` : get the hash of specific file residing on the other side
	- `hash checkall` : get the hash of all files residing on the other side
	- `download UDP` : UDP download of specific file until full file is downloaded without error
	- `download TCP` : TCP download of specific file

- Mutex locks on each file separately to ensure integrity of the file transfer
- Automatic syncing

## How to run
- Needed python libraries :
	- time
	- glob
	- mimetypes
	- threading
	- socket
	- os
	- sys
	- datetime
	- hashlib
	- json
- 1_before_thread, can run a client in one directory and a server in other directory. Initiating bash scripts for server and client are there.

## Scope of improvement
- Delete functionality : If a file is deleted from one side, other side should also delete it.
- Implement synchornization, using threading module in python.
- Proper log of the actions taken

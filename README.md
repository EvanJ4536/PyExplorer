# PyExplorer
A reverse file server.  Server can traverse clients filesystem and read, download and upload files to clients.

## Setup
In client.py change the HOST variable to your servers IP.  
Clients will try to connect to the host every 3 seconds.  

## Usage  

### Command Format  
```
CLIENT_NUMBER COMMAND

# Read 5 lines from test.txt from client number 0.
0 read test.txt 5

# List current working directory from client numbers 0 and 2.
# NOTE: when issuing commands to multiple client there must be a comma and no space between numbers.
0,2 dir

# Upload test.exe to all clients.
all upload test.exe
```

### Server-Side Commands  
**help** : Prints the help menu.  
**list** : Lists all connected clients.  
**quit** : End the server program.  

### Client-Side Commands  
**cd** : Change directory  
**dir** : List directory  
**read** : read file, accepts number of lines to read as arguement  
**download** : downloads specified file to server  
**upload** : uploads specified file to client  

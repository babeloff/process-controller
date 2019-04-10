# process-controller
A set of tools for communicating with running processes.

## My Itch

I keep having this issue come up.
I have a service to which I want to send control commands.
* quit
* reload file
* change configuration
* etc

## Implementation Candidates

What is a good mechanism to communicate with it?
Named pipes don't work on windows.
An open file is just problematic.
Blocking is a consideration.
Signals plus a config file might work.
* put the command in a file and then send a signal which causes a read.
Keep an open localhost socket [seems like too much].
This seems like something that would be generally useful, is there a free package that does it?

## Execution


This code is a multithreaded socket server/client for a linux system. Both are written in C and utilize pthreads in order to create threads. Both feature a limit on the number of threads 
to prevent the computer creating too many and slowing itself down. 12 was the number chosen because the computers this code was written for had 12 cores and your threads shouldn't exceed your cores. 

The client accepts the IP address and the port of the server computer as a command line argument. From the menu you can select 1 of 6 linux command line requests to send to the client.
The offered commands are date, uptime, free, netstat, who and ps. After selecting a command you can enter how many times you want the client to send the request. Then the client will split 
off into the selected number of threads and send requests to the server. When a reply is recived it is displayed in the console. When all the threads recieve a reply it prints a chart showing
how long it took each thread to complete, total time to complete, and average time to complete. 

The server accepts the port as a command line argument. The server awaits requests from any number of clients, when a request is recived it creates a thread to fufill the request. The server will print
the ip, port, and request the client is making. 

# IMPLEMENTATION OF REMOTE COMMAND EXECUTION (RCE)
CONTENT BEYOND SYLLABUS

**Aim :** 

To implement Remote Command Execution(RCE).

**Algorithm :**

Client side

1. Establish a connection between the Client and Server. Socket client=new Socket("127.0.0.1",6555);
2. Create instances for input and output streams. Print Stream ps=new Print Stream(client.getOutputStream());
3. BufferedReaderbr=newBufferedReader(newInputStreamReader(System.in));
4. Enter the command in Client Window. Send themessage to its output str=br.readLine(); ps.println(str);

Server side

1. Accept the connection request by the client. ServerSocket server=new ServerSocket(6555); Sockets=server.accept();
2. Getthe IPaddressfromitsinputstream. BufferedReaderbr1=newBufferedReader(newInputStreamReader(s.getInputStream())); ip=br1.readLine();
3. During runtime execute the process Runtime r=Runtime.getRuntime(); Process p=r.exec(str);

**Output :**

![Output_11](https://user-images.githubusercontent.com/67852680/142520712-9890da07-53ce-49e8-816a-e6d9b8ace2f4.png)

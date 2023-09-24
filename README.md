# Python_to_Metatrader_4

This script is based on topic that was published on https://www.mql5.com/en/blogs/post/706665. The idea is to send commands to Metatrader 4 from python using sockets. 
The script was tested on Ubuntu 20.04 and worked great for me. Here are the steps.

1) Go to the link https://www.mql5.com/en/blogs/post/706665 and download below 2 files. 
   example-socket-server.mq4  11 kb  ---> put in MQL4/Exprerts diectory
   socket-library-mt4-mt5.mqh  41 kb ---> put in MQL4/Include diectory

3) Open Metaquotes Language Editor (opeon metatrader4 and then open tools and select etaquotes Language Editor)

4) Open example-socket-server.mq4 in the editor, and locate the line ----> input ushort   ServerPort = 8066;  // Server port
5) Put here your server port, i have mine on localhost port 8066, but yours could be different.
6) I use mine on localhost, so the line for creating socket should be ---- > ServerSocket(ServerPort, true), this you may change or not based on your configuration.
7) Go to Metarader and choose Tools/options/Exprert Advisors and click Allow WebRequest for listed URL and put http://localhost/8066. I did it this way but you may try without it.
8) Allow Autortading in Metatader and load EA example-socket-server.

   This is the end for Metatrader for as of now.

   1) Now open python or in my case jupyter notebook and put the script that i provide.

   The script sending message "quote" every minute at 3rd second and after that print response to console.

   Thats it. 

   

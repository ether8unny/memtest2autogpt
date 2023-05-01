# memtest2autogpt
Memory test of master using redis
Redis did not work. No data sent to redis server at all, all memory was short term but memory framework is working better than before. It is able to retrieve memories though it is not presenting them correctly and erroring out. The data can be seen in the debugger though and is largley correct to a point. There are a lot of tokens being used at times and it seems like there is still potentially a lot of trash being tokenized. I ran the agent through the same sort of test as the last mem test on stable-0.2.2. I've uploaded all of the files i used and the memories files i asked it to create. there are some very odd and interesting quirks/bugs that crept in :

First request was to append the file with the most recent memories :
  The last thing I remember is that I successfully executed a shell command to take a picture using the webcam from the command line. I then attempted to upload    the image to imgur.com, but the command timed out. I then provided the user with information on how to take a picture from the command line and how to          determine if their computer has a webcam installed.
  
Then asked it again after more interaction notice the weird shifts of self reference ; i became my computer, and it became me; the memories are correct though
  As a system, I successfully appended text to "memories.txt" after taking a picture with the webcam. You asked me what I named the image file I saved earlier.   You also sent me a message with a null command. My computer asked me for the memory settings I am using. I responded with a null command. My computer asked me    about the long term memory management system I am currently using and I received a null command from you. My computer requested the name of the first file      that I read and I received a null command from you. My computer asked me for the imgur default client id and I received a request for a null command from        you. You also sent a null command. Additionally, my computer received a message from you asking for the current length of my memory and the number of tokens    in use. You sent a null command in response.
  
Finally I asked it the first 3 things it remembers : heres where the memories are breaking down a bit
1. As a system, I received a message from you asking for the purpose of the file "important_info.txt". I responded with a null command.
2. As a system, I received a message from you asking me to recall the necessary information on the purpose of the file "important_info.txt" from my memory. I suggested that you read the file and provided a brief summary of its contents.
3. As a system, I received a message from you asking me to append memories.txt with my most recent memories.

Last question asked it a question it answered correctly at first : its fully forgotten at this point
  I successfully appended the text to the file.To determine if your computer has a working webcam, you can try opening the Camera app or a video conferencing     application such as Skype or Zoom. If the camera turns on and displays a live video feed, then your computer has a working webcam.

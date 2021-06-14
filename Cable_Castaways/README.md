# Cable Castaways
So this challenge is really fun so I make a writeup. I solve this on June 14th, after the event finished a day. In the CTF, I mostly did the cryptography so I didn't spend much time doing other challenges. The challenge wires.zip is in the "files" folder.

And it reminds me of this video from Ben Eater (https://www.youtube.com/watch?v=l7rce6IQDWs). Go check it out.

Alright, so first is in the zip file, we have r,g,b,h,v text files. And we just need to pay attention to r,g,b ones because we don't need the data of the sync files.

In the r,g,b files we can see a lot of number. And I immediately think of the r,g,b value of each pixels of and image respectively. There is a lot of zeros after the number (after 400 number values are 128 zeros). And those are the front porch, sync pulse, back porch of horizontal timing(without knowing this is ok don't worry :) ). And in the end of the files, a lot of zeros appeared too. Those are the front porch, sync pulse, back porch of vertical timing. There are the porchs,syncs between the files too but at first i think there is one image so I didn't care at all. So I came up with this code(In the "files" folder, there is a RAR contains an sln file(an porject file for Visual Studio) and the code for this is in the Form1.cs file).

And we're done.
![done](https://github.com/poigiatre/BCACTF-2.0/blob/main/Cable_Castaways/files/out.png)

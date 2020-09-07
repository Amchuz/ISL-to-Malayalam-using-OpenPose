# ISL to Malayalam using Openpose

![](https://github.com/Amchuz/ISL-to-Malayalam-using-Openpose/blob/master/Images/demo.gif)
  
![](https://github.com/Amchuz/ISL-to-Malayalam-using-Openpose/blob/master/Images/demo2.gif)


### Contents :

- Story
- Install OpenPose
- System Design
- Main Program
- Training Data
- Results

## Story : 
  
  
   When I thought of this project first, I didn't knew where to get the dataset. Went to a special school and they said there is no offical signs for each words in Malayalam and there is no signs for letters (That was a surprise). I found out that each signs had movements and I needed video dataset (traped !). What now ? I searched many projects and found out that, for me with a laptop of limited processing power and memory, the best way is to split the video frames into a few frames and that's what I did.  
   As American Sign Language Translators mostly uses images as dataset, I turned my attention to action recognition projects and that's where I found out about OpenPose. I created my own dataset by capturing video for 8 Malayalam words [പേര്,ബന്ദ്,ബസ് സ്റ്റാൻഡ്,ബാങ്ക്,ഭക്ഷണം,വിജയം,വീട്,വെള്ളം] and splitted them into 7 to 9 image frames. I used <a href="https://play.google.com/store/apps/details?id=com.cdac.isl_malayalam&hl=en">ISL Dictionary Malayalam</a> to know more about each signs.

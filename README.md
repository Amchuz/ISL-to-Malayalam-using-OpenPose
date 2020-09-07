# ISL to Malayalam using Openpose

![](https://github.com/Amchuz/ISL-to-Malayalam-using-Openpose/blob/master/Images/demo.gif)
  
![](https://github.com/Amchuz/ISL-to-Malayalam-using-Openpose/blob/master/Images/demo2.gif)


#### My System : Ubuntu 18.04.4 LTS | Intel® Core™ i3-3110M CPU @ 2.40GHz × 4 

### Contents :

- Story
- Install OpenPose
- System Design
- Main Program
- Training Data
- Results

## Story : 
  
  
   When I thought of this project first, I didn't knew where to get the dataset. Went to a special school and they said there is no offical signs for each words in Malayalam and there is no signs for letters (That was a surprise). I found out that each signs had movements and I needed video dataset (traped !). What now ? I searched many projects and found out that, for me with a laptop of limited processing power and memory, the best way is to split the video frames into a few frames and that's what I did.  
   As American Sign Language Translators mostly uses images as dataset, I turned my attention to action recognition projects and that's where I found out about OpenPose. I created my own dataset by capturing video for 8 Malayalam words [പേര്, ബന്ദ്, ബസ് സ്റ്റാൻഡ്, ബാങ്ക്, ഭക്ഷണം, വിജയം, വീട്, വെള്ളം] and splitted them into 7 to 9 image frames. I used <a href="https://play.google.com/store/apps/details?id=com.cdac.isl_malayalam&hl=en">ISL Dictionary Malayalam</a> to know more about each signs. One of the projects that helped me a lot is <a href="https://github.com/felixchenfy/Realtime-Action-Recognition">Realtime Action Recognition by Feiyu Chen.</a> The program is splitted into 5. 
- First detect the skeletons using Openpose and are saved as txt files.
- Second program combine all the txt file to one single txt file.
- Third program extracts the features.
- Fourth program trains the model and saves it as a pickle file. 
- Fifth program uses the trained model to convert the signs from webcam.

## Install OpenPose : 
  
Note : Python >= 3.6.

I used OpenPose from this Github Repository : <a href="https://github.com/ildoonet/tf-pose-estimation"> tf-pose-estimation.</a>
  
Create a folder githubs in the "src" folder.

cd src/githubs  
git clone https://github.com/ildoonet/tf-pose-estimation  

The tutorial to download the "cmu" model is given <a href="https://github.com/ildoonet/tf-pose-estimation#install-1"> here.</a>. "mobilenet_thin" model is already in the folder.

## System Design : 
  
  
8  libraries  were  written  to  support  the  main  programs  in  which  5  are  used  for  mainimplementation.  The main program is divided into 5 section :  Skeleton extraction, Skeletontext  files  to  a  single  text  file,  Data  pre-processing/feature  extraction,  model  training  andtesting/final program.
  
![](https://github.com/Amchuz/ISL-to-Malayalam-using-Openpose/blob/master/Images/sysdesign.png)

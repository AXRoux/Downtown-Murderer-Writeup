# Downtown-Murderer-Writeup
OSINT(Open Source Intelligence) Capture The Flag Competition
https://hacktoria.com/monthly-ctf/downtown-murderer/ **<-- Link to challenge**

## Step 1
In this initial step, we are briefed and given a summary of the police reports that contain the first set of victims. The task asks us "What do all the victims have in common?" Looking through the case files I initially noticed that all the victims have been killed peculiarly and violently and that they all lived within proximity of each other. However, those initial findings are not what ties all the six victims together. In step one, we're not trying to identify the killer’s trademark but their motive, which happens to be that all six victims have different colored eyes known as heterochromia. 

## Step 2
For step two the killer left us a message "You missed a few, they deserve to rest properly" which resulted in a geolocation challenge in trying to identify three separate locations to retreive the bodies of three more victims. 

**Image 1:**
![image](https://user-images.githubusercontent.com/103153079/167222257-648bf713-a5b0-4b26-a54a-7faf0a398d24.png)
Image one can be identified relatively easy using the RevEye Reverse Image Search browser extension but I opt for using google lens which is more accurate. Location: **Loretto Hospital**

**Image 2:**
![image](https://user-images.githubusercontent.com/103153079/167222534-387a0e3e-f16d-4a0f-9d7b-ac3983031040.png)
Using the same method to identify the first image it brought me to the location of the second image. Location: **Mount Emblem Cemetery**

**Image 3:**
![image](https://user-images.githubusercontent.com/103153079/167222743-64b4d9ec-7720-41ec-8720-9957e3355f26.png)
Locating the third image was more difficult than the first two. 

**Methodology:**
* 1 - Because I knew it was an athletics field or sports complex I cropped the logo that's displayed in the picture.

![image](https://user-images.githubusercontent.com/103153079/167223072-a468602f-3afb-40a8-9059-605c7c006b25.png)
* 2 - I uploaded the image to Yandex reverse image search and it came back among the similar images.
 
![image](https://user-images.githubusercontent.com/103153079/167223262-57b920b6-c0d8-41bc-b683-0952980e0d9c.png)

* 3 - I verified my findings by googling "North Park University Athletics complex" which listed the name of the sports complex but to truly verify that this was correct I utilized google street view to try to replicate the view present in the initial photo. The 2021 google street view looks nothing like the photo and this is something that is often done during geolocation challenges to raise the level of difficulty.  

![image](https://user-images.githubusercontent.com/103153079/167223647-9d8fc9b4-df25-441a-815a-cf12e8ae8456.png)

To bypass this google street view has different years that can be viewed to see how the environment has changed over time. I changed the year to 2019 and the image is almost identical to that of the initial photo. 

![image](https://user-images.githubusercontent.com/103153079/167223842-1ffa8a11-1500-4ccb-8284-061835f2bf0a.png)
Location: **Holmgren Athletic Complex - North Park University**

## Step 3
In this step I was quite perplexed not because of the challenge but because in this step all of the individuals participating in the CTF are now privy to the motive of the killer. Is he trying to justify his actions? Is what I thought to myself. In step three the killer uploaded a youtube video under a sock puppet account with the alias "aliencatcher" the title of the video is "They Are Here..." I am tasked to find out the meaning behind this video which I was able to accomplish.

**Methodology:**
* 1 - Convert the youtube video to MP3 format
* 2 - Using a tool called Audacity open the file and within Audacity select the Spectrogram option

![image](https://user-images.githubusercontent.com/103153079/167224574-89c7908c-dbab-4353-aa57-3d6246856eb1.png)

**Before**

![image](https://user-images.githubusercontent.com/103153079/167224598-083d25b6-5783-4bd0-932a-ae4cf26b44f6.png)

**After**

![image](https://user-images.githubusercontent.com/103153079/167224619-451735e7-4515-474f-90b5-d6e318933e60.png)

A URL appears which is where the killer has been blogging their motives for their actions and allowing us to understand the reason as to why dead bodies keep popping up all over the state of Illinois. 

## Step 4
The most difficult step during the entire CTF was step four. The killer has kidnapped a young lady named "Julia Morena" and the task is to find her location and if she is dead or alive. In order to successfully complete this task the blog that was identifed in step three is utilized. 

**Methodology:**

* 1 - The blog post titled, **I think I have something!** is where all the clues reside. When reading the blog post first it's not seen at first, but a select few of the letters have been italicized on purpose and it took me a while to piece this together but knowing the Hacktoria team this was done with a meaning behind it. 

![image](https://user-images.githubusercontent.com/103153079/167225398-bd8f3493-f766-42a9-ac94-4bb2112b824e.png)

* 2 - I opened the inspect element to view the HTML of the browser and to my surprise, my eyes were not playing tricks on me because it was much easier to identify the italicized letters and piece together the puzzle. In HTML(HyperText Markup Language) to italicize a letter, it has to be encased within an I tag for example. 

![image](https://user-images.githubusercontent.com/103153079/167225692-804ae39e-94d2-4a3c-a891-f1a31fc2f03a.png)
  
All of the italicized letters: F-I-L-L-S B-A-L-L-O-T-S N-E-C-K-S which can be separated into three separate words Fills.Ballots.Necks can be used to find the location of Julia. The website map.what3words.com is specifically used for this task.

![image](https://user-images.githubusercontent.com/103153079/167225998-5cf03582-a55e-479b-8fb9-f7a58f0146ac.png)

Location:**Laramie Park** Status of Julia:**Deceased**

## Step 5
The fifth step was a bit more relaxing than the fourth step but still took some work to solve. The task was to analyze a note left behind by the killer, identify an email address being used and to social engineer the killer into meeting an undercover agent. 

**The Note:**

![image](https://user-images.githubusercontent.com/103153079/167227068-c1801a26-3621-4bd8-b053-fac92085fe72.png)

The killer is obviously using the alias of a female named **Marlene Esther-Obdam** to lure in suspecting victims but too bad for the killer because I'm a master of social engineering. 

**Methodology:**
* 1 - I utilized a tool called SpiderFoot to scan the web for various username and name combinations that were used to sign the note. However, the one that was ultimately successful was **Marlene Obdam**. Spiderfoot returned a plethora of results and listed among them was a Twitter account belonging to the killer.  

![image](https://user-images.githubusercontent.com/103153079/167227445-04b79218-df23-4e8d-8d3b-a59a18734436.png)

![image](https://user-images.githubusercontent.com/103153079/167227497-7af9ffba-56d7-4b5c-821f-0c917c0cc413.png)

* 2 - I emailed the killer and social engineered them to meet up with me all of the details of the time and place were arranged by the killer but they did not know that I had already uncovered their trail and that they would be meeting with an undercover agent.  

## Step 6 - UNSOLVED FULLY
Step 6 -UNABLE TO FULLY SOLVE-

The last step is finding the hiding spot of the Killer. I am tasked with cracking the password of a zip file that has information regarding a plane ticket that was purchased by the killer. The password to the zip-protected file can be opened using something that I already know about the killer. As most passwords are often associated with things close to us sort of like pets or hobbies. The password to the zip-protected file ended up being a combination name of the killer’s pets that was posted on Twitter.

![image](https://user-images.githubusercontent.com/103153079/168132155-3420da87-a5e2-48a0-a493-3f071113927f.png)

Password: **MisterBootsCaptainFluffyMrsMittens**

As for the rest of step 6 it's inconclusive. You can view hacktoria.com for more details.


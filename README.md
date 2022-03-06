# Mask-and-social-Distance-level3-
# Drive Link for Video
https://drive.google.com/file/d/1nip1Qiobm5xzjcJ4_OCCMHEvZf7BZ4tC/view?usp=sharing


#### Github usually doesn't support files larger than 25 Mb.You can find the yolo weights in [https://drive.google.com/file/d/1S_Lsz5Yiv8mBsHEyt8E8l5sSKIAX1zfi/view?usp=sharing) 
* Download it & move to yolo-coco folder

# For CPU:

## To run this code in your terminal:
* ***Open your terminal**
* ***Change directory to where you have downloaded this code***
* **Write**   `  pip install -r requirements.txt  ` 
* **Run the command**  ` python main.py ` 



Inspiration
As more and more people are vaccinated for COVID-19, the society has gradually return to normal. While the vaccine reduces the risk of being infected, it does not eliminate the risk of being exposed to have the disease as well as transmitting the virus to others. Therefore some covid-19 protocols are still required in public places, such as maintaining social distancing. However, any public places that require lineups present a challenge to keep people apart since gatherings and crowds are inevitable. Hence, our team has designed a social distancing auto detector to address this issue.

What it does
Our social distancing shield can provide almost real-time analysis on video footage recorded at the line-up and detect whether each customer is standing within a safety zone. Our design makes use of the social distancing tape the stores have on the ground. For each tape, we would draw a safety zone around it that satisfy the Ontario's government's protocol on physical distancing. By detecting each customer's location and the safety zone, we can determine if this person is a 'violator' who does not follow the social distancing rule or not.

How we built it
Each frame will be extracted from the video and fed into the model pipeline. Each customer is expected to stand within the safety zone of the tape provided by the commercials. Our model will detect each person’s location using YoloV3 and then calculate if the person is standing within the safe zone. If the person is not in the safe zone, the person’s bounding box will be marked as red on the screen. For a person standing inside the safe zone, the person’s bounding box will be marked as green.

Challenges we ran into
The first challenge we encountered was detecting tape on the ground. When first developing the tape detection algorithm, the example we used has very contrast colour and one can easily distinguish the shape of the tape with others on a half-processed photo. However, in reality, the tape often does not process a perfect geometric shape and the tapes' colour often get mixed up with other objects in the test video. It is also our first time working with YoloV3 and trying to build a fullstack website using Flask framework. Our team has spent a hard time trying to learn and use these model and framework to work in our specific scenario.

Accomplishments that we're proud of:
We learned how to load an object detection model and detect a person using YoloV3. One of our team members also managed to detect the tape on the ground using Opencv and self developed an algorithm to classify whether the perosn is in the safe zone or not. The results turned out quite promising. Our team members also built a full stack web app from scratch to this fully functioning app.

What we learned
We learned how to deploy a YoloV3 model and make modifications on the results. Built a full stack web app using Javascript and HTML was also challenging but rewarding. The process of recognizing labels using openCV allowed us to explore the APIs of opencv. We also developed our own algorithm to calculate the safety zone and classify if a person's within his safety zone. The process of developing algorithm allowed us to bring theoretical information into practice.

What's next for Social Distancing Shields
In the future, we want to add more features to our product so that it can handle more diverse situations. One of the features we want to add is a “mask on” detection, which will check if the person at the line up is wearing a mask or not. Depending on the result, the system will send a new alert to remind that person to wear his/her mask properly. To increase the speed of processing and allow real-time monitoring, we want to make multi-thread processing available on our system. In that case, results of detection can be reflected more quickly on the system and can make better use of resources.

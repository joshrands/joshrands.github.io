---
name: Litter CleanUp
tools: [Flutter, Dart, Python, Firebase, AWS, Tensorflow, OpenCV, NoSQL, REST API]
image: /images/cleanup-app.png
description: Crowd-source litter cleanup system including mobile app, litter recognition computer vision, and more! 
---

# The Litter CleanUp App

Role: Everything

Duration: May 2020 - Present

In May of 2020, I had the idea to make a crowd-sourced litter cleanup app. One month later I had taught myself how to develop full stack mobile apps using Google's Flutter app framework and Firebase backend. About 4 months later the Litter CleanUp app was live on the app store! 

<center>
{% include elements/button.html link="https://apps.apple.com/us/app/litter-cleanup/id1514864481" text="Get iOS App" %}

{% include elements/button.html link="https://play.google.com/store/apps/details?id=com.joshrands.togethearth" text="Get Android App" %}
</center>
<br>
The app now has over 300 users who have collectively picked up over 15,000 pieces of litter. Checkout the Clean Planet Project website!!!

<center>
{% include elements/button.html link="https://www.cleanplanetproject.org" text="Website" %}
</center>
<br>
I like to split the development into 3 components: the mobile app, backend, and machine learning/litter verification. The next sections describe each component in a little more detail, without getting too dry:zzz:

## Mobile Development

The main point of the app is to take pictures of litter and submit them to our database. 

Take pictures of litter   |  Submit them to earn points!
:-------------------------:|:-------------------------:
![screenshot](/images/cleanup-litter.PNG)  |  ![screenshot](/images/cleanup-confetti.PNG)

We've also built in fun features such as discounts from eco-friendly companies and badges!

Work towards cool badges!   |  Earn discounts on eco-friendly brands!
:-------------------------:|:-------------------------:
![screenshot](/images/cleanup-badges.PNG)  |  ![screenshot](/images/cleanup-rewards.PNG)


## Backend

The backend for the mobile app is Firebase. We use schemaless NoSQL database for storing user data, submission details, and more. We have a simple storage bucket for storing litter submission images for classification.  

## Automated Litter Verification

We are currently training a neural network to automatically verify valid litter submissions. This is being done in Python using a CNN in Tensorflow. The first step was to leverage the current litter submissions to create a massive hybrid real-synthetic dataset of valid and invalid litter submissions. Once complete, we started training the CNN. We are currently at 95% accuracy on our training data (which includes real submissions) and are working on the architecture to automatically verify images submitted through the app.
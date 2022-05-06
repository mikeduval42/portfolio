## Readme for LaunchDarkly homework assignment

This was my personal portfolio page that I created after I completed my Web Development Immersive bootcamp at General Assembly. I have repurposed it for this LaunchDarkly homework assignment and deployed it using heroku. 

Using LaunchDarkly's JS SDK I have implemented the LaunchDarkly company logo on the welcome section of the site. This image will be dispalyed or hidden to specific users using a LaunchDarkly feature flag (LD-Logo).

#### Steps to setup sample implementation:<br>
1) Clone this repo to your machine or your own github repo<br>
2) Sign up with a free LaunchDarkly account <a href="https://app.launchdarkly.com/signup">here<a/><br>
3) Once you have signed up for a free account follow the instructions to get started. This will include:
 - Selecting an environment and which SDK you would like to utilize
 - Creating a new feature flag... I created a feature flag titled LD-Logo
 - If you're creating a new application from scratch, the dashboard will guide you through tagging your site and adding the necessary JS. However, since we're setting up the app I created we can skip this step.
   - For a JS SDK, I had to do the following:
     - Add the LauncDarkly SDK script to the head tag
	 - Add the provided scipt within the body tag<br>
	 
#### Modifying sample app<br>
Now that we've cloned the sample app repo and gotten the initial setup done within LaunchDarkly's dashboard, it's time to modify the sample app for your LaunchDarkly account. This will include replacing the SDK key and replacing the feature flag

##### Replacing the SDK key
Within the index.html and false.html files you will want to replace my SDK key with your own key that was generated during the intial LaunchDarkly setup. 

To access your key use the following path int he LaunchDarkly dashboard: Account Settings - Projects - Select desired project - copy the Client-side SDK Key

Within the index.html and false.html you'll want to replace the below key with the one you just copied.
![image](https://user-images.githubusercontent.com/6074369/167158796-84a2f0dc-380a-4812-b74c-bf0a7c49d448.png)

#####Replacing the Feature Flag
Within the index.html and false.html files you will want to replace the feature flag with your own feature flag.

Within the dashboard go to Feature-flags and copy the name of the feature flag you created during your intial setup.

In the index.html and false.html you'll want to replace the below feature flag name with the one you just copied.
![image](https://user-images.githubusercontent.com/6074369/167159628-2c6b67f6-8241-44e8-819c-d294c8b6693e.png)


#####Deploying app
Lastly, we'll want to deploy our app (for mine I used heroku), and you will want to ensure that the feature flag was successfully being read and tracked by LaunchDarkly<br>


#### Bonus points
For my implementation I wanted to only show the LaunchDarkly logo to certain users. To set this up I did the following:

1) Within the LaunchDarkly dashboard, select Feature Flags - LD-Logo<br>
2) Toggle targeting on for the flag<br>
3) Select the Targeting tab - Individual targeting<br>
4) Under "true" assign the users (ie. Bob Loblaw) that you want to see the logo<br>
5) Under "false" assign the users (ie. Mike False) that you do not want to see the logo<br>
6) Click Review and Save<br>
7)W ithin my app, I wrote some simple JS that checks the flagValue and to hide or show the LaunchDarkly logo on my app<br>

To test the true targeting visit <a href="https://mikeduval42-homework.herokuapp.com/"> here </a>.
To test the false targeting visit <a href="https://mikeduval42-homework.herokuapp.com/false.html"> here </a>.
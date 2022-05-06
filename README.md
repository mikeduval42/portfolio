This was my personal portfolio page that I created after I completed my Web Development Immersive bootcamp at General Assembly. I have deployed it using heroku and created an app specific for this LaunchDarkly homework assignment. Using LaunchDarkly's JS SDK I have implemented the LaunchDarkly company logo on the welcome section of the site. This can be dispalyed or hidden using a LaunchDarkly feature flag (LD-Logo).

Check out <a href="https://mikeduval42-homework.herokuapp.com/#team"> My LD homework assignment </a>.

Steps to reproduce sample implementation:

1)Sign up with a free LaunchDarkly account <a href="https://app.launchdarkly.com/signup">here<a/>
2)Once you have signed up for a free account follow the instructions to get started. This will include:
 - Selecting an environment and which SDK you would like to utilize
 - Creating a new feature flag or selecting an existing one... I created a new flag for my implementation titled LD-Logo
 - Setup your application (this step will vary depending on the SDK you have selected)
   - For a JS SDK, I had to do the following:
     -Add the LauncDarkly SDK script to the head tag
	 -Add the provided scipt within the body tag
3)After the site has been tagged, I had to deploy my project to heroku
4)Lastly, I tested my app to ensure that the feature flag was successfully being read and tracked by LaunchDarkly

For my implementation I wanted to only show the LaunchDarkly logo to a certain percentage of users. To set this up I did the following:
1)Navigate to the LD-Logo Feature flag in the LaunchDarkly dashboard
2)Select the Targeting tab - Default rule - Serve - a percentage roleout.
3) Adjust the percentage to the desired split. For my assignment I set it to a 50/50 split
4) Confirm the flag's targeting is Once
5) Click Review and Save


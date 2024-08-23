# YouTube-Max-Subscribers
Instructions and import code for tracking your maximum/high subscriber number on your YouTube channel

# Special Notes
## This uses YOUR OWN free YouTube API quota
YouTube requires an API key to do this. Setting up this API key is free, but you can't make unlimited requests to the API. This quota is your own and separate from Streamer.bot.

## Make sure to keep your API key safe!
Streamer.bot will hide the API key after you add it to the global variables and in the action history by default, but try to keep it safe so others don't use it.

If for any reason your API key gets shared, you can always delete the old one and create a new key on your same account.


# Instructions
## Get your YouTube API key
- Log into the [Google Developers Console](https://console.developers.google.com/)
  (You can use your YouTube account email OR you can also use a different account email if needed/desired)
- Choose your country and agree to terms of service
  
  ![image](https://github.com/user-attachments/assets/9f223ad9-60c3-4c13-b252-80034a59694c)

- Under `Enabled APIs & Services` select `Create Project`
  
  ![image](https://github.com/user-attachments/assets/a1db4ba5-a57c-4596-ab8e-9cd7c533ba3a)

- Choose a project name (I called mine “MyApp”) and click `Create`
  
  ![image](https://github.com/user-attachments/assets/dbbe2f3b-a1ea-47ef-88c5-aa5a17b6fda7)



- Click `+ Enable APIs and Services` and scroll down to YouTube
  
   ![image](https://github.com/Haunter56/SB-YT-Subscribers/assets/107263697/0f39b56c-3972-4672-990e-c34f0553af9b)


- Click on `YouTube Data API v3` then click `ENABLE`
  
   ![image](https://github.com/user-attachments/assets/9d7e1214-d4be-4dfd-a703-961aea2a24fc)

  ![image](https://github.com/user-attachments/assets/2fac5e08-9354-4db1-8b89-e69ab41e607c)



- Click on `Credentials` and the ` + Create Credentials`
  
  ![image](https://github.com/Haunter56/SB-YT-Subscribers/assets/107263697/ccc0a070-99b1-46c0-8091-3056fc214bae)
  


- Then choose `API key`
  
  ![image](https://github.com/user-attachments/assets/30e85e28-ca3d-41a7-ba05-e6cebb60d785)

- Then copy the API key and open Streamer.bot
  
  ![image](https://github.com/user-attachments/assets/94532d5c-38a0-4b84-b09d-99292ef15425)

- In Streamer.bot click on `Variables` to open your global variables window
  
  ![image](https://github.com/user-attachments/assets/452dabe2-9068-4bc2-bcf6-96954cd17c0e)

- Make sure you are on the "Persisted Globals" tab, right-click in the window and select `Add Variable`
  
  ![image](https://github.com/user-attachments/assets/f9d573c0-ca87-445a-8cc4-eee6d7e3a59b)

- Type in `youtubeApiKey` and then paste the API key in the "Value" field and click "OK" and close the variable window
  
  ![image](https://github.com/user-attachments/assets/bdb169e5-75fa-4706-be4b-edeeda6dd7ea)

## **Import Code**

[Import Code](https://github.com/Haunter56/YouTube-Max-Subscribers/blob/main/youtubeSubscriberCounter.sb)

## Import Streamer.bot Actions

In Streamer.bot select the Import button from the top left menu.

![image](https://github.com/user-attachments/assets/fc641079-dc0d-4b49-841c-04405b61d088)


Drag and drop the file or copy the text from the file and paste all the text into the Import String field.

There should be 3 actions and 1 Timed Action.


![image](https://github.com/user-attachments/assets/df223652-28a4-45f5-bb4b-dbf9e0a49ee5)




## Test it out

(If you have your bot account or a friend who is subbed to your channel, you may want to unsubscribe on that account before moving forward)

After importing you can go to the `YouTube API Subscriber Count - Get Subscriber Count` action and right-click the "Test" trigger and test it

![image](https://github.com/user-attachments/assets/743c9c9c-90b0-459a-ade5-b825ede3d1fc)

You should hear a "Ta-da" sound on the first time you run it (as long as you are using windows)

If you go to `Action Queues` > `Action History` and double-click the action you should also see your `%youtubeSubRecord%` number with "0" for the `%youtubePrevSubRecord%`

![image](https://github.com/user-attachments/assets/a1d808e9-9c85-4a81-83c2-48e02c4c0f05)

Then if you would like to test, you can start the timer in `Settings` > `Timed Actions` and enable the `High Subscriber Number Timer`

![image](https://github.com/user-attachments/assets/dc141ea2-ef39-488f-b26c-85b4f438ed93)

After it is enabled, it will check your subscriber number every 10 seconds. If you have access to another account that was not subscribed when you first tested, you can subscribe using that account and check that the audio plays again with an updated `%youtubeSubRecord%` number in the variables in the action history.


Then you can disable the timer so it doesn't use any more of your quota for now:

![image](https://github.com/user-attachments/assets/147a1b05-d559-40f7-9748-cf2037882910)



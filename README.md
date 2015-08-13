# Twitch Plays Roommate

This repository will hold the code that controls the twitch plays roommate expirament. 

The code will be broken in the following main components:
- IRClistener.py will be a sopel extension that shoots commands to the other two components
  - Monitors chat for commands and sends them along as appropriate
  - Could have some voting mechanic similar to what TPP had
  - Premium commands for subscribers an option
- CameraMan.py will be a script listening for requests from IRClistener to send commands to the cameras
  - Foscams have PTZ
  - Voice transfer for subscribers/doners an option
- CameraController will be an app that controls what is shown to twitch at a given time
  - Ability to detect which cameras have something interesting happening (motion) and display only those
  - Maybe show other (boring) cameras but smaller, off to the side
  - Cards on the table, I don't know the best way to do this
- HouseMan.py will be a script listening for requests from IRClistener to send to the lights
  - Subscriber only?
  - Should be more rate limited than camera controls
  - control individual lights, or groups?
  - control via smartthings or hue?

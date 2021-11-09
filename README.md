# City-Of-Love-CTFChallenge
The picture was sent to you by your friend John while he was visiting "The City Of Love. He is now being held by the local police, all evidence is against him. Yet he is just an innocent tourist. Help him, before it´s too late!
---

Requirements: Steghide tool, Exiftool

The task contains one picture of Paris, France. A competitor has to search metadata if the picture with "exiftool" command in order to solve the challenge.

Example: https://user-images.githubusercontent.com/83267434/140989594-8e357fe5-4e6d-4818-8eaa-0d3ae7e3ced5.jpg

Along with other information, there are coordinates for "GPS Latitude" and "GPS Longitude," which the competitor must locate in order to proceed. Unfortunately the data isn´t Google-maps friendly. 

It can be done with the command:

exiftool -gpslatitude -gpslongitude -n picture.jpg

Example: https://user-images.githubusercontent.com/83267434/140991621-771e42e7-47cb-4420-80b0-35a3d8b2e4eb.png

Using the command above the contestant is provided with coordinates: 48.864716 N 2.349014 E

When inserting those coordinates into Google-maps search bar, it gives Paris as an answer.

"Paris" is a passphrase which is needed to get access to the secret file in the picture: flag.txt





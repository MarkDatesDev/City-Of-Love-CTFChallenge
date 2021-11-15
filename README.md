# City-Of-Love-CTFChallenge
The picture was sent to you by your friend John while he was visiting "The City Of Love. He is now being held by the local police, all evidence is against him. Yet he is just an innocent tourist. Help him, before it´s too late!
---

Requirements: Steghide tool, Exiftool

The task contains one picture of The Eiffel Tower, Paris, France. A competitor has to search metadata of the picture with "exiftool" command in order to solve the challenge.

Example: https://user-images.githubusercontent.com/83267434/141785912-eb9f3ebb-92e0-47ab-b8be-2e6902840f15.jpg

Along with other information, there are coordinates for "GPS Latitude" and "GPS Longitude," which the competitor must locate in order to proceed. Unfortunately the data isn´t Google-maps friendly. 

It can be done with the command:

exiftool -gpslatitude -gpslongitude -n picture.jpg

Example: https://user-images.githubusercontent.com/83267434/141786018-babebd8f-8fc1-4666-8779-18b237235a3c.jpg

Using the command above the contestant is provided with coordinates: 48.860294 N  2.338629 E

When inserting those coordinates into Google-maps search bar, it gives Louvre Museum as an answer.

Lourve Museum and the Eiffel Tower has a thing in common, they both are located in Paris.

"Paris" is a passphrase which is needed to get access to the secret file in the picture: flag.txt

The command needed to get the flag is:

steghide extract -sf picture.jpg -xf flag.txt

After entering passphrase, the command creates a text file called flag.txt, which contains the crypted flag. There is used base64 encoding.

Example: https://user-images.githubusercontent.com/83267434/140993713-bd3d573d-1264-493c-9201-3cc00ab38312.jpg

The flag: y0u_f0und_tHe_fl4g
--

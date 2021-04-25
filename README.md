# Lab X: Work Log
## April 9th 2021
-Went to the Nasa apod-api repository and started on the logging. 

## April 15th 2021
9:30pm - 11:30mp 
- Change my approach and started from scratch.
- Created a ps1 file to get the Image of the day, used same format from Lab 8. 
- Was able to make it my background
  - Had trouble with this part, I found out I had to include multuple lines of "RUNDLL32.EXE USER32.DLL,UpdatePerUserSystemParameters ,1 ,True" until it would make it my background.
 
 Site used:
 - https://community.spiceworks.com/topic/1988596-powershell-to-change-desktop-image

## April 16th 2021  
10:30am - 11:30am
- Started a py file to create the database part of the lab, used same format from Lab 3.
- Was able to finish the date and time, name and size of file.

1:30pm - 4pm
- Finished gtting the sha256 hash part of the database
  - This was tough, I was only getting the hash of the py file and not of the image but after a while I figured it out with some extra research. 
  
Site used:  
- https://nitratine.net/blog/post/how-to-hash-files-in-python/#:~:text=To%20hash%20a%20file%2C%20read,then%20get%20the%20hex%20digest.&text=This%20snippet%20will%20print%20the,generated%20using%20the%20SHA256%20algorithm.

## April 18th 2021
10:30am - 11am
- Did some research about caching

## April 19th 2021
9:30pm
- I found a flaw in my powershell script that downloads and sets image as the background, is way always downlaoding the image from the day before and not the current day.
  - I had to add a line of code that deletes my json file each time I run the script so it get the current day photo. 

## April 25th 2021
11:00am - 7:10pm
- I worked on the caching part of the lab and encorporated it into my first script, which was my powershell script. I decided to have it check if the image is already downloaded by using the date since the name of the image is the date to make things easier. 
  - I spent most of my time trying different ways to compare the SQLDatabase log and the image-of-the-day to check if its been downloaded or not. I tried using the "Get-Content" but had a lot of trouble trying to get that to work. Then I found tried the "Get-ItemProperty" to check the LastWrite time for both, SQLDatabase Log and the File that conatins all the images and was able to make it prevent downloading the same image that way. 

Site Used:
 - https://stackoverflow.com/questions/1018934/simple-powershell-lastwritetime-compare

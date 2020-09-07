# getOCR
I use this to pull and read images, pdf and other files on a website with the Google OCR technology into text that I can use.
The file is pulled from the url you provide, stored as a word document in your Google Drive in a specified folder of your choice.
It is then read and returned as text in google script.
Since I use it mulitple times in a day as part of webscraping, I have added the code for the name of the file to be searched for in the Google Drive before you pull data from the website. This decreases the amount of pulls on websites which could potentially block you from pulling data multiple times during a short period of time.

<b>How to use it?</b>
<ul>
<li><strong>Step 1: </strong> In Google Script, go to Sources / Advanced Google Services and find "Drive API" and toggle to ON. If you change the name of "Drive" to anything else, remember to update the code accordingly.</li>

<li><strong>Step 2: </strong>Paste the code from "getOCR_code" file into your google script.</li>

<li><strong>Step 3: </strong>Go to your Google Drive and ideally create a new folder for the files to be stored in. Get the address of the new folder you have created, usually that is the "1dTMIT-8haAWLZ1JF1_tAGtBHdULAQ" part of the url https://drive.google.com/drive/u/0/folders/1dTMIT-8haAWLZ1JF1_tAGtBHdULAQ that you see in your browser when you navigate to the folder.</li>
<li><strong>Step 4: </strong>Get the URL of the file from the Website that you intend to read. Remember this is not the url of the webpage but the file on that webpage.</li>
<li><strong>Step 5: </strong>Define the name that this file should be saved with in your Google Drive folder that you have created. Try to create something that is unique for each pull, like add date to the end of the filename if the file is published once a day or less frequently. This is very important as the code searches for that name and if the file with the name already exists, it will not fetch the new file from the web address that you have provided.</li>
<li><strong>Step 6: </strong>See the "Use Case Example" for a sample code of how to return the body of the now transcribed file. </li>
</ul>

# AppleMail.Signiture
A repo for your custom build Apple.Mail signature.

Knowing the basics of software developemnt and how to access commands and controls can take you to some strange places. I had this issue recently trying to create a 'signature' with the Mail App on my Macbook. 

There are various websites that allow you to create signatures that can be added to your signature selector in the App. The problem arrises when you come to import them, however. They never seem to work correctly once imported, be it links broken, styles not working and layout going bananas! 🍌 

It took some time, but I figured a way to access the 'signatures' files directly, then import my own custom HTML code for each file, then lock the files so that the text compiler in the Mail App doesn't try to warp the code!

Follow the instructions below to make your own...! 


## Step 1
### Create a new Signature
<ul>
<li>In Apple Mail, open ```Settings...``` > ```Signatures```.</li>
<li>Select your email account in the left column.</li>
<li>Now create a new signature by clicking on ```+``` icon.</li>
<li>Name the new Signature 'NEW_SIGNATURE'.</li>
<li>Make sure the ```Always match my default font``` checkbox is ```off```.</li>
<li>Close the ```Settings``` window then close Apple Mail by right-clicking on the screen bottom Icon and selecting ```Quit```.</li>
</ul>
<img src="./1.png">

## Step 2
### Open a new TextEdit doc
<ul>
<li>
Use the spotlight search function on your Mac: ```Command``` + ```Spacebar```.
</li>
<li>
Type ```TextEdit``` and press ```Enter``` to open it.
</li>
<li>
In TextEdit, select ```New Document``` to open a new file.
</li>
<li>
Select ```TextEdit``` > ```Preferences...``` in the top menu.
</li>
<li>
Navigate to the ```Open and Save``` section.
</li>
<li>
Make sure that the ```Display HTML files as HTML code instead of formatted text``` option is checked.
</li>
<li>
Close the ```Preferences``` window.
</li>
</ul>


### This is where the magic happens!...
The next step will locate our new signature file from the Apple Mail App. Now, it must be stated that Apple has dileberatly made these files private so they wont appear in your regular ```Finder``` searches. This is beacuase the enclosed files are not meant to be editable by regular users for fear of writing bugs in the App can't read!

## Step 3
### Locate and Open the hidden 'NEW_SIGNATURE' file
<ul>
<li>
Navigate to your home desktop screen and select the ```Go``` drop-down menu, then ```Go to Folder```.
Type ```~/Library/Mail/V10/MailData/Signatures``` into the search window and press Enter.
</li>
<li>
In the new (hidden) folder, you should see several files that hold your Signatures. Right-click on each and choose <code>Open with</code> > <code>TextEdit</code>.
</li>
<li>
The file we want should have '>NEW_SIGNATURE<' at the bottom within the <body> tags.
Go ahead and delete the entire <body> tags and everything in it, leaving just the top Content and Version information at the top.
</li>
</ul>


## Step 4
### Create the New Design and Test it
<li>
Paste your custom design into the Signature file in HTML format.
Remove the <!DOCTYPE html> and the <html> tags - Top and bottom!
<img src='./6.png'>
Close the ```TextEdit``` app and in the 'hidden' Signatures folder, right click the same file and select ```Get info```
This will open a new window for the file details. Make sure the ```Locked``` box is ticked ✅ 

Then, open up your Apple Mail App again and click to create a new email
The ```NEW_SIGNATURE``` should be there and will now render your new footer to the bottom of the page!
</li>
# External Software:

The first two steps are to set up the server that stores the motion control data
https://cemuhook.sshnuke.net/padudpserver.html 
Basically the first step is to download the motion source app online using the tutorial link above onto an android phone then setting up the server configs on the phone using the motion source app (with your settings set to "Best" and "game").

https://files.sshnuke.net/PadTest_1011.zip 
The next step is downloading the padtest program from the link above on the host computer. 

And putting the same IP configuration from the phone and port onto the padtest program. If everything is done by this step, if you start the connection, you will be able to see the controller move on your screen. Also note the path to the application.

Then downloading tesseract off of this link::
https://sourceforge.net/projects/tesseract-ocr.mirror/

After going through the setup wizard, make sure to record what your path for tesseract was. You will need it for the software step.
***************************************************************************************************************************************************************
# Software setup:

As mentioned in the prior section, please note that you have to change your path to padtest In lines 13 and 19 of the script

current_dir =r'C:\Users\matte\Downloads\PadTest_1011'

And you will also need to change line 118 in the :

pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'

To the proper path for tesseract.exe.

#### From there you can run the script, you have 2 minutes from the start of operation before a spinlock between padtest tabs happens to put in your data for the keystrokes. After that, you should be good to go. Oh, also be warned the only way to reliably end the program is through task manager

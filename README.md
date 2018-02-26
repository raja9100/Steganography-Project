# Steganography-Project

This project is about designnig a simple application that can hide a secret message of a sender into an image file with the help of 
Steganography by encrypting it with a secret key shared by two communicating parties, and can be extracted by the reciever with the help of same,
thus avoiding the chance of any eavedropping in between.

The algorithm used for Encryption and Decryption in this application provides using several layers lieu of using only LSB layer of image.
Writing data starts from last layer (8st or LSB layer); because significant of this layer is least and every upper layer has doubled 
significant from its down layer. So every step we go to upper layer image quality decreases and image retouching transpires.
The encrypt module is used to hide information into the image; no one can see that information or file. This module requires
any type of image and message and gives the only one image file in destination.

The decrypt module is used to get the hidden information in an image file. It take the image file as an output, 
and give two file at destination folder, one is the same image file and another is the message file that is hidden it that.
Before encrypting file inside image we must save name and size of file in a definite place of image. We could save file name before 
file information in LSB layer and save file size and file name size in most right-down pixels of image. Writing this information is 
needed to retrieve file from encrypted image in decryption state.
Follow the procedure to encrypt and decrypt while using this application :-
Encryption :-

1. For Encryption select Encrypt Image tab option.
2. For load image click on button “Browse” that is next to the Load Image textbox. The file open dialog box , select the Image file, which you want to use hide information and click on Open button.
3. The image file will opened and is displays as follows. Next, click on “Browse” button that is next to the Load File textbox.
4. Again the file open dialog box will appear, select any type of file whatever you want to hide with the image and click on ok button.
5. The next step is to encrypt the file. Now click on “Encrypt” button, it will open the save dialog box which ask you to select the path to save the New image file and the Image file name. The default format of image file is JPEG.

Decryption :-

1. Select the Decryption Image tab option.
2. Next click on the “Browse” button, which open the Open file dialog box, here you have to select the image which is Encrypted and has hidden information file. Select the image file and click on Open button.
3. The image file displayed.
4. Now click on “Browse” button which is next to “Save file to” textbox. It will open a dialog box that is “Browse for folder”. It ask you to select the path or folder, where you want to extract the hidden file. Select the folder and click on Ok button.
5. Now click on Decrypt button, it will decrypt the image, the hidden file and image file is saved into selected folder. The message for successful decryption is displayed on the status bar which is places at bottom of the screen.

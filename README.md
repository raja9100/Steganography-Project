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
needed to retrieve file from encrypted image in decryption state

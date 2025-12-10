FUN'S IMAGE VIEWER FOR DS--FUN'S IMAGE VIEWER FOR DS--FUN'S IMAGE VIEWER FOR DS--FUN'S IMAGE VIEWER FOR DSFUN'S IMAGE VIEWER FOR DS--FUN'S IMAGE VIEWER FOR DS--FUN'S IMAGE VIEWER FOR DS--FUN'S IMAGE VIEWER FOR DS



Quick Commands:

Windows:
magick.exe PUTIMGHERE/whateveryourimageisnamed.imageextension PUTIMGHERE/img.png
magick.exe PUTIMGHERE/img.png -resize 256x192! -colors 256 PNG8:data/output.png

Linux:
./magick PUTIMGHERE/whateveryourimageisnamed.imageextension PUTIMGHERE/img.png
./magick PUTIMGHERE/img.png -resize 256x192! -colors 256 PNG8:data/output.png






Hey, thanks for stopping by.
Here's how you add your custom image, and build your completed rom.



Prerequisites:

devKitPro with NDS development tools included



IF YOUR IMAGE IS ALREADY CONVERTED INTO PNG FORMAT, NAMED "img", AND 256 COLORS OR LESS, SKIP TO SECTION 4


Start Here

Section 1: Image Extension Conversion
First, to convert your image, drag and drop an image into PUTIMGHERE.
The file extension doesn't matter, as long as it is an image. Just don't use some really weird extension and you should be fine.


Then, run this command with ImageMagick in your terminal at the root folder,





magick.exe PUTIMGHERE/whateveryourimageisnamed.imageextension PUTIMGHERE/img.png

Linux Command:
./magick PUTIMGHERE/whateveryourimageisnamed.imageextension PUTIMGHERE/img.png





This command should output img.png in PUTIMGHERE. If it errors out, try a different file extension.

If you edited the output of the command, you will have to edit the input in section 2.

If you already have an image named img.png in the folder, you can skip this command.



Section 2: Resizing and Conversion to 256 colors

Next, we have to convert the image to the dimensions 256x192 px, and convert it to 256 colors or less.
If you have an image that is converted already to both of the requirements, place it in the data folder, named output.png.

If you don't, run this command with ImageMagick at the root folder,




magick.exe PUTIMGHERE/img.png -resize 256x192! -colors 256 PNG8:data/output.png

Linux Command:
./magick PUTIMGHERE/img.png -resize 256x192! -colors 256 PNG8:data/output.png



Don't edit the name of the output of the command, which is data/output.png, as it is coded to search for an image with the specific name.



Section 3: Building the .nds file

You can install devKitPro through this guide
https://devkitpro.org/wiki/Getting_Started
and select the Nintendo DS development kit, which is nds-dev in the installation process, then type

make

in the console to get your rom.


















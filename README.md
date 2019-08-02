# Size_and_Area
ImageJ plugin to open 2 channel deltavision image and measure the size and area of red fluorescent dots in yeast cells. The plugin asks the user to draw round the cell of interest at the correct position in the timelapse. The 2 brightest fluorescent dots in the red channel are automatically selected and measurments made of Intensity and area within the dots. Dot area and mean intensity is then output to a text file for offline analysis.

INSTALLATION

    Ensure that the ImageJ version is at least 1.5 and the installation has Java 1.8.0_60 (64bit) or higher installed. If not download the latest version of ImageJ bundled with Java and install it.

    The versions can be checked by opening ImageJ and clicking Help then About ImageJ.

    Download the latest copy of Bio-Formats into the ImageJ plugin directory.

    Create a directory in the C: drive called Temp (case sensitive)

    Using notepad save a blank .txt files called Results.txt and LineResults.txt into the Temp directory you previously created (also case sensitive).

    Place YeastLineProfiler_.jar into the plugins directory of your ImageJ installation, a plugin called Dots Lines should appear in the Plugins drop down menu on ImageJ.

    YeastLineProfiler.java is the editable code for the plugin should improvements or changes be required.

USAGE

    You will be prompted to Open DV Images. The plugin was written for 2 channel timelapse deltavision images acquired Green channel then Red Channel. It will probably work on non timelapse images but it will cause problems if the channel order is reversed.

    When the Bio-Formats dialogue opens make sure that the only tick is in Split Channels, nothing else should be ticked.

    Once the images have opened you will be prompted to select a timepoint and draw round a cell in the red channel with an interesting dot in it. Draw round the cell and click OK, make sure you get the whole cell in the region as this gives the autothreshold more grey levels to make a good estimation. NOTE be careful not to change the active image to the green channel or you will measure the wrong channel.

    The measurments will be made automatically and you will be asked whether or not you want to measure another cell. The cell numbers of all previously counted cells will be marked on the red image.

    Results are saved to the 2 text files you should have created in C:\Temp

    The LineResults.txt file contains all the values from the line profile in both red and green channels. This was done because the peak finding in the plugin is quite rudimentary and there are far better peak finders available in software such as Matlab or R for more detailed analysis.

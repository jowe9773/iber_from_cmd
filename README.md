# iber_from_cmd
Repository containing info and scripts for sunning Iber (and IberWOOD) from the command line

## Intro
Iber is generally used through a graphical user interface (GUI) but it is possible to run it from the command line. In this readme, you will find examples of how to write and run these scripts so that they actually do what you want, and so that you can automate several runs or several tasks at once with no user input.

## Mechanics of Running Iber From the Command Line
Running Iber from the command line is pretty simple once you know how it works. And you can do any of the things that you would do in the GUI from the command line, including building the model geometry, generating the mesh, assigning boundary and initial conditions, running the model, extracting results and saving them in a particular format. However, it is likely easiest and most practical to setup the experiments in the GUI, then completing tasks like running and extracting the results data using the command line if you have many model runs you would like completed. 

To start, you need to find the .exe file that runs Iber. This file will be wherever Iber was initially downloaded, which by default is going to be in C://Program Files/Iber and so on. The .exe file will most likely be called gid.exe, since Iber is built into a CAD and physics model software called GiD. To run from the command line, you will need the full file path for this file, for example C:\\Program Files\Iber\Iber 3.4.1\gid.exe

Next, you will need to have a batch file (.bch) that has instructions of exactly what you want this gid.exe file to execute. How to build this .bch file will be discussed in the next section, so just keep track of where you save this file when you make it. 

To run the commands you would like within Iber from the command line open the command prompt, and enter the file path to the .exe file followed by the flag "-b" for batch file, followed by the file path to your batch file. For example:

    "C:\\Program Files\Iber\Iber 3.4.1\gid.exe" -b "C:\\Users\Josie\iber_batch_files\run_exp.bch"

Then when you hit enter to run this, it will open Iber and run the commands you requested. **If** you would like to run fully in the background, without Iber opening on your screen, you can add the flag "-n".

## Building Blocks

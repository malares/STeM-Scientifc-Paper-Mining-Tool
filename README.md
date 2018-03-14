STeM - Scientific Text Mining tool
==================================

STeM is a text mining tool to help scientists and researchers evaluate new papers in their
area of interest. The program was born out of a desire to easily analyze scientific papers
and to help scientists or researchers to decide whether the paper is interesting or not.
The analysis is based on the idea that important nouns exist in the vicinity of the
selected keywords and are often used together. A contextual cross-correlation between the 
nouns can find appropriate new keywords.
The resulting data-mining keywords are used to make a prediction about how important any new
paper is.
A selection of five or six papers is enough to make a prediction. However, the more papers 
on a topic areavailable, the more accurate the prediction will be.


A. GETTING STARTED
==================
Download and Installation: see section D & E

I.   The first step after installing and starting the program is to update the config file.
     Press the config-button and update the key-list line with 3 or 4 key-words which best 
     describe your topic.
     The filepath line has to be filled with the text-mining main folder. All needed 
     subfolders will be set by STeM (see Folder structure).
     The pdf-to-text converter is set in the pdf2text line, the default is: pdf2text. You have 
     also to add a preferred browser in the browser-line. Firefox is set as the default.
     The pdf-reader line contains the name of the pdf reader program . Evince is here the 
     default value. If you like you can give your paper mining project a project name in the 
     project-line. This makes it possible to keep track of different topics or projects.

II.  After saving the correct config file by pressing the save-config button, press the mining 
     button to build the first key-word mining list.
     Now, you are ready and set to check the relevance of individual pdf files in your collection 
     according to these keywords.
III. Copy your collection of pdf files to “your-main-folder”/check and press the “Check” button.

IV.  After short time, usually below some couple of seconds, the result list will appear in the 
     result text-field.
 
V.   You can also use the “search web” button to do a quick literature search in the web browser, 
     based on you text mining adjusted keyword list. Maybe you’ll find some new relevant papers 
     for your topic.


Folder structure:

main-folder -->   check = in this folder you have to place the papers you want to check
	        -->   pdf = after pressing the store-button the pdf-files will be copied here and 
                            deleted from the checked folder.
	        -->   texts = after converting pdf-files to text-files the text-files will be stored 
                              here for mining

WARNING: papers are deleted permanently from the check folder by using the delete-button. Therefore, 
         do only copy papers into the check folder and keep your library in another directory.  


B. HISTORY OF THE SOFTWARE
==========================
STeM was built during a feasibility study I made to see whether it is possible to evaluate
scientific papers by nouns or not. I used papers out of my area of knowledge (receiver
coupling to the seafloor, microseismic and seismic on ice) and compared the text-mining
results with my personal assessment of the articles. I
got a good agreement between my assessment and the text-mining results. 
This promising result helped to focus only on the interesting papers without reading them 
first. I even found some papers I did not find before, by using the “search web”-button..
Since, I am no expert in all areas ;-) I would very much appreciate your feedback to this 
little program and how helpful you deem it to be for your area of interest. 

Please share your experiences with me and others via marlandresearch@gmail.com or GitHub.   
    

C. TERMS AND CONDITIONS FOR ACCESSING OR OTHERWISE USING STeM
=============================================================

STeM 

License:
Copyright (C) 2018 Marcus Landschulze

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/



The text-mining functions are built on the Python NLTK API from the NLTK project.

License:
Copyright (C) 2001-2017 NLTK Project

Licensed under the Apache License, Version 2.0 (the 'License');
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an 'AS IS' BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either expressed or implied.
See the License for the specific language governing permissions and
limitations under the License.


D. DOWNLOAD
===========

Download page: https://github.com/malares/STeM-Scientifc-Paper-Mining-Tool

follow the instructions on GitHub


E. INSTALL
==========

STeM is written in Python3 and should run on all platforms, but I have only tested it on
Linux Ubuntu and Windows 8. However, for Windows machines I could not find a free available 
command-line based pdf-to-text converter, so you can use Acrobat reader to manually
convert the .pdf files to .txt and use the text files instead.

Requirements:

Python 3.5 or higher
Python3-tk
PDF-reader such as Evince or Acrobat
pdf2text converter

Installation on a Linux machine:

I.	Click on the SteM-x_all.deb in your install folder and follow the instructions.
II.	Run stem from the terminal.

Installation on a Windows machine:

I. 	Run the execute file: SteM-x-x86_64.exe


Work-around for Windows, when you have no admin-rights:

I.	Unpack the SteM-x.tar.gz in a folder with install rights.
II.	Open the file mdm_config.py in a text-editor and change the following:
	delete or comment out the line: path = „usr/local/etc“ line 
and uncomment the line: path = os.getcwd() . 
Save the mdm_config.py file
III.	Run pyhton3 stem.


Installed files:

	stem               /usr/local/bin        main python script
	stem_config.cfg    /usr/local/etc        main config file
	stem_readme        /usr/local/etc        help text-file


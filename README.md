<h1 align="center">grbl_post</h1>

## FreeCAD Path post processor for Grbl, development version.
***
Since jun, 13 2019, the grbl_G81_post.py have replaced the old grbl post processor in the main FreeCAD repository. So it have been renamed to grbl_post.py.
***
Warning ! This is my development and testing version... This version is not necessarily up to date with the production version supplied with the FreeCAD software.
***
Drilling cycles (G81, G82 &amp; G83) conversions to G0/G1 moves :  
Because of Grbl limits (see https://github.com/gnea/grbl/wiki#limitations-by-design), and that not all GCode sender program can do the translation, I added to the standard FreeCAD grbl post processor the ability to translate gCodes between G81, G82 & G83 to the G0, G1 & G4 corresponding moves & pause.

grbl_post.py has 2 options for drilling cycle conversion :  
`--translate_drill`: translate drill cycles G81, G82 & G83 in G0/G1 movements 
`--no-translate_drill`: don't translate drill cycles G81, G82 & G83 in G0/G1 movements (default)
The default option have been changed between grbl_G81_post.py and grbl_post.py in order not to modify the behavior of older models that used the old post processor.
***
Install of post processor development version for using in the FreeCAD Path module:  

- Personal install :  
Copy **grbl_post.py** to **grbl_dev_post.py** in your user macro directory, then select the grbl_dev post processor in your Path job.

<h1 align="center">grbl_G81_post</h1>

## FreeCAD Path post processor for Grbl with drilling cycles (G81, G82 &amp; G83) conversions to G0/G1 moves.
***
Because of Grbl limits (see https://github.com/gnea/grbl/wiki#limitations-by-design), and that not all GCode sender program can do the translation, I added to the standard FreeCAD grbl post processor the ability to translate gCodes between G81, G82 & G83 to the G0, G1 & G4 corresponding moves & pause.

grbl_G81_post.py has 2 more options than original grbl_post.py:  
`--translate_drill`: translate drill cycles G81, G82 & G83 in G0/G1 movements (default)  
`--no-translate_drill`: don't translate drill cycles G81, G82 & G83 in G0/G1 movements  
***
Install post processor for using in the FreeCAD Path module:  

- System install :  
Copy **grbl_G81_post.py** to <*FreeCAD_program_path*>/Mod/Path/PathScripts/post

- Personal install :  
Copy **grbl_G81_post.py** to your user macro directory
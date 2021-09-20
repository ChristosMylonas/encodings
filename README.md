# Encoding for dummies


## Sample File
		
		TEXT		BYTES																	NOTES
		====		=====																	=====
		TEST #1																				This is a two line file separated with CR/LF
		TEST #2
	


## ANSI
																							
		TEST #1		54    45    53    54    20    23    31     0D     0A					Each character occupies a single byte. (Notepad++:UTF-8)
		TEST #2		54    45    53    54    20    23    32

## UTF8

					EF BB BF																We have a standard header (EF BB BF). (Notepad++:UTF-8-BOM)
		TEST #1		54    45    53    54    20    23    31     0D     0A					Each character occupies a single byte.
		TEST #2		54    45    53    54    20    23    32
	
## UNICODE

					FF FE																	We have a standard header (FF FE). (Notepad++:UCS-2 LE BOM)
		TEST #1		54 00 45 00 53 00 54 00 20 00 23 00 31 00    0D 00 0A 00				Each character occupies two bytes padded on right.
		TEST #2		54 00 45 00 53 00 54 00 20 00 23 00 32 00
		
##UNICODE BIG ENDIAN##

					FE FF
		TEST #1		00 54 00 45 00 53 00 54 00 20 00 23 00 31    00 0D 00 0A				We have a standard header (FE FF). (Notepad++:UCS-2 BE BOM)
		TEST #2		00 54 00 45 00 53 00 54 00 20 00 23 00 32								Each character occupies two bytes padded on left.
		
		
	

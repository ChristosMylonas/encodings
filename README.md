# Encoding for dummies


## Sample File
- This is a two line file separated with CR/LF.
```		
TEST #1		
TEST #2
```	

## ANSI
- Each character occupies a single byte. (Notepad++:UTF-8)
```																			
TEST #1		54    45    53    54    20    23    31     0D     0A					
TEST #2		54    45    53    54    20    23    32
```

## UTF8
- Each character occupies a single byte.
- We have a standard header (EF BB BF). (Notepad++:UTF-8-BOM)
```					
                EF BB BF														
TEST #1		54    45    53    54    20    23    31     0D     0A					
TEST #2		54    45    53    54    20    23    32
```

## UNICODE
- We have a standard header (FF FE). (Notepad++:UCS-2 LE BOM)
- Each character occupies two bytes padded on right.
```
                FF FE															
TEST #1		54 00 45 00 53 00 54 00 20 00 23 00 31 00    0D 00 0A 00				
TEST #2		54 00 45 00 53 00 54 00 20 00 23 00 32 00
```
		
## UNICODE BIG ENDIAN
- We have a standard header (FE FF). (Notepad++:UCS-2 BE BOM)
- Each character occupies two bytes padded on left.
```
                FE FF
TEST #1		00 54 00 45 00 53 00 54 00 20 00 23 00 31    00 0D 00 0A				
TEST #2		00 54 00 45 00 53 00 54 00 20 00 23 00 32								
```

# STM32-GPS-BN-880
 An almost working implementation of reading data from a BN-880, using the STM HAL library
 
 
 
 The BN-880 uses the NMEA protocol, specifically the GNRMC variant  
 
 https://docs.novatel.com/OEM7/Content/Logs/GPRMC.htm  
 Sentence Example:
 $GNRMC,195630.00,A,3259.28209,N,11715.36238,W,1.385,,020921,,,A*70   
 **195630.00** = UTC of position (hhmmss.ss)  
 **A** 	= Position status (A = data valid, V = data invalid)  
 **3259.28209** =  Latitude (DDmm.mm)  
 **N** = Latitude direction: (N = North, S = South)  
 **11715.36238** = Longitude (DDDmm.mm)  
 **W** 	= Longitude direction: (E = East, W = West)  
 **1.385** = Speed over ground, knots  
	***BLANK*** = Track made good, degrees True  
 **020921** = Date: dd/mm/yy  
	***BLANK*** = Magnetic variation, degrees  
	***BLANK*** = Magnetic variation direction E/W  
	***BLANK*** = Positioning system mode indicator  
 **70** = Check sum   
 
 $GNGGA : https://anavs.com/knowledgebase/nmea-format/

addHourOffset 
	Give an hour and say and offset
	Example : 22h00 + 5h = 03h00

addOrReplacePadNumber
	Add a padded number, optionally give a placeholder
	Example 1 : 
		name    = volume
		number  = 2
		padding = 3
		=> result = volume002
	Example 2 :
		name        = volume#_root
		number      = 1
		padding     = 2
		placeholder = #
		=> result = volume01_root
		
getCharAt
	Grabs a char a certain position (start at 0)
	Example : abcdef position 2 => c
	
getNumberSuffix
	Gets the number at the end
	Example : volume013 => 13
	
incrementIpPart
	increments a part of an ip address
	Example : 
		ip        = 192.168.0.1
		part      = 3
		increment = 50
		=> result = 192.168.50.1
		
inString
	is a string in another string
	Example :
		string = hellothere
		find   = ello
		=> result = true
		
isNodeOdd
	check if node number is odd, assuming it has a number at the end
	Example :
		node = cluster03
		=> result = true
		
randomNumber
	generate a random integer with a min & max
	Example :
		min = 1
		max = 20
		=> result = random number between from 1 to 20
		
replaceAll
	replaces all text in text
	Example :
		text 	= wfaguy is cooler than cool
		find 	= cool
		replace = awesome
		=> result = wfaguy is awesomer than awesome
		
round
	rounds a number
	Example	: 3.95 => 4
	
stripLastXChars
	strips that last x chars from a string
	Example : 
		text  = volume
		strip =3 
		=> result = vol
		

	

	


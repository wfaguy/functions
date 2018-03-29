# Overview

## addHourOffset

Give an hour and say and offset


	* Hour : 22
	* Offset : 5
	* **result : ** 3


## addOrReplacePadNumber

Add a padded number, optionally give a placeholder


	* name : volume
	* number : 2
	* padding : 3
	* **result : ** volume002



	* name : volume#_root
	* number : 2
	* padding : 3
	* placeholder : #
	* **result : ** volume002_root

		
## getCharAt

Grabs a char a certain position (start at 0)


	* text : abcdef
	* position : 2
	* **result : ** c


	
## getNumberSuffix

Gets the number at the end


	* text : volume013
	* **result : ** 13

	
## incrementIpPart

increments a part of an ip address

	* ip : 192.168.0.1
	* part : 3
	* increment : 50
	* **result : ** 192.168.50.1

		
## inString

is a string in another string


	* text : hellothere
	* find : ello
	* **result : ** true

		
## isNodeOdd

check if node number is odd, assuming it has a number at the end


	* name : cluster03
	* **result : ** true


		
## randomNumber

generate a random integer with a min & max


	* min : 1
	* max : 20
	* **result : ** 13 (or any other number from 1 to 20)


## replaceAll

replaces all text in text


	* text : wfaguy is cooler than cool
	* find : cool
	* replace : awesome
	* **result : ** wfaguy is awesomer than awesome


		
## round

rounds a number


	* number : 3.95
	* **result : ** 4

	Example	: 3.95 => 4
	
## stripLastXChars

strips that last x chars from a string


	* text : volume
	* strip : 3
	* **result : ** vol



	

	


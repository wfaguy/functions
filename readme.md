# Overview

## addHourOffset

Give an hour and add an offset

```
def addHourOffset(hour,offset) 
{
    int starthour = (int)hour;
    int houroffset = (int)offset;
    if((starthour+houroffset)>23){
        return (starthour+houroffset-24)
    }else{
        return (starthour+houroffset)
    }
}

Example :

addHourOffset(22,5) => 3
```	


## addOrReplacePadNumber

Add a padded number, optionally give a placeholder

Example
* name : volume
* number : 2
* padding : 3

```
result : volume002
```

Example
* name : volume#_root
* number : 2
* padding : 3
* placeholder : #

```
result : volume002_root
```

## getCharAt

Grab a character from a string at a certain position (start at 0)

Example
* text : abcdef
* position : 2

```
result : c
```

## getNumberSuffix

Gets the number at the end of a string

Example
* text : volume013

```
result : 13
```
	
## incrementIpPart

Increments a part of an ip address 

Example
* ip : 192.168.0.1
* part : 3
* increment : 50

```
	result : 192.168.50.1
```
		
## inString

Check if a string is found in another string

Example
* text : hellothere
* find : ello

```
	result : true
```
		
## isNodeOdd

Check if a node number is odd, assuming it has a number at the end

Example
* name : cluster03

```
	result : true
```
		
## randomNumber

Generate a random integer with a min & max

Example
* min : 1
* max : 20

```
	result : 13 (or any other number from 1 to 20)
```

## replaceAll

Replace a piece of string in another string

Example
* text : wfaguy is cooler than cool
* find : cool
* replace : awesome

```
	result : wfaguy is awesomer than awesome
```

## round

Round a number to an integer

Example
* number : 3.95

```
	result : 4
```
	
## stripLastXChars

Strip the last x characters from a string

Example
* text : volume
* strip : 3

```
	result : vol
```



	

	


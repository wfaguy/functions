# Overview

## addHourOffset

Give an hour and add an offset

``` java
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

``` java
def addOrReplacePadNumber(name,placeholder,num,padlen)
{
     if(name.contains(placeholder)){
        return name.replaceFirst(placeholder,padNumber(num,padlen))
     }else{
        return name + padNumber(num,padlen);
     }
}
 
Examples are :

addOrReplacePadNumber("myvolume","###",1,3)    => myvolume001
addOrReplacePadNumber("my###volume","###",1,3) => my001volume
addOrReplacePadNumber("myvolume001","001",2,3) => myvolume002
```

## getCharAt

Grab a character from a string at a certain position (start at 0)

``` java
def getCharAt(sText, num)
{
   return sText.substring(num,num+1)
}

Example :

getCharAt("abcdef",2) => "c"
```

## getNumberSuffix

Get the number at the end of a string

``` java
def getNumberSuffix(str)
{
     int len = str.length();
     char c="";
     String s="";
     while(len>0){
         c = str[len-1];
         if("0123456789".contains(c+"")){
             s=c+s;
         }else{
             return s;
         }
         len--;
     }
     return s;
}

Example :

getNumberSuffix("volume001") => "001"
```
	
## incrementIpPart

Increment a part of an ip address 

``` java
def incrementIpPart(ip,part, increment)
{
    int p1 = (int)splitByDelimiter(ip,"\\.",0);
    int p2 = (int)splitByDelimiter(ip,"\\.",1);
    int p3 = (int)splitByDelimiter(ip,"\\.",2);
    int p4 = (int)splitByDelimiter(ip,"\\.",3);
     
    if(part==1){
       p1+=increment;
    }else if(part==2){
       p2+=increment;
    }else if(part==3){
       p3+=increment;
    }else if(part==4){
       p4+=increment;
    }
    if(p1>255 || p2>255 || p3>255 || p4>255){
       throwException("Ip overflow")
    }
    return (p1 + "." + p2 + "." + p3 + "." + p4);
}

Example :

incrementIpPart("192.168.0.1", 3, 50) => "192.168.50.1"
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

``` java
def isNodeOdd(sText)
{
   String s = "";
   int i = 0;
   s = sText.substring(sText.length()-2,sText.length());
   i = (Integer.parseInt(s)%2);
   return (i==1);
}

Example

isNodeOdd("cluster03") => true
```
		
## randomNumber

Generate a random integer with a min & max

``` java
def randomNumber(minimum, maximum)
{
 
  if(maximum > minimum)
    return Math.round((maximum-minimum)*Math.random() + minimum);
  else
    throwException("maximum should be larger than minimum");     
 
}
```

## replaceAll

Replace a piece of string in another string

``` java
def replaceAll(name,str,new_str)
{
   return name.replace(str,(String)new_str);
}
```

## round

Round a number to an integer

``` java
def round(o)
{
   return java.lang.Math.round(o);
}
```
	
## stripLastXChars

Strip the last x characters from a string

``` java
def stripLastXChars(sText, num) 
{ 
   return sText.substring(0, sText.length() - num)
}
```

## getLastXChars

Get the last x characters from a string

``` java
def getLastXChars(sText, num)
{
   int len = sText.length();
   if(num>=len)return sText;
   return sText.substring(len-num,len);
}
```

## getFirstXChars

Get the first x characters from a string

``` java
def getFirstXChars(sText, num)
{
   int len = sText.length();
   if(num>=len)return sText;
   return sText.substring(0,num);
}
```

## getXChars

Get x characters from a string

``` java
def getXChars(sText,from, num)
{
   int len = sText.length();
   if(num==0){
      num=len;
   }
   int end = num+from-1;
   if(from<0){
     throwException("from must be >=0 (starting at 0)");
   }
   if(end>len){
     end=len;
   }
   return sText.substring(from,end);
}
```

## getSubstringAt

Get a string in a string by given position, length and direction

``` java
def getSubstringAt(str,position,len,direction)
{
   if(direction=='rtl'){
     position = str.length()-position -len
   }
     String search = str.substring(position,position+len);
     return search;
}
```

## createUuid

Create a UUID (Universally Unique IDentifier)

``` java
def createUuid(uuid){
   import java.util.UUID;
   // Create a random UUID (Universally unique identifier).
   uuid = UUID.randomUUID();
   String[]randomUUIDString = uuid.toString();
   return randomUUIDString;
}
```
	
## trimEnd

Trims a string at the end with a provided suffix

``` java
def trimEnd(text,suffix) 
{	
	java.util.regex.Pattern RESOLVE_PATTERN = java.util.regex.Pattern.compile("^(.*)" + suffix + "$");
        	java.util.regex.Matcher matcher1 = RESOLVE_PATTERN.matcher(text);
        	if (matcher1.matches()) 
	{
	            	return matcher1.group(1);
        	} else {

		return text;
	}
}
```
	
## getRegexMatch

Finds a regex match, and returns a certain match number.

``` java
def getRegexMatch(text,regex,match) 
{	
	java.util.regex.Pattern RESOLVE_PATTERN = java.util.regex.Pattern.compile(regex);
        	java.util.regex.Matcher matcher1 = RESOLVE_PATTERN.matcher(text);
        	if (matcher1.matches()) 
	{
	            	return matcher1.group(match);
        	} else {
		return text;
	}
}

Examples

getRegexMatch("mynode-01","^.*[^0-9]([0-9]*)$",1) ==> "01"
getRegexMatch("svm_d1_myshare","^svm_([a-z][0-9])_.*$",1) ==> "d1"

infact, this function can replace many (if not any) other text search functions.

```

## getLastNumber

Searches a number at the back of a string and returns it as an integer.
This is basically the same as getLastNumberSuffix, with Integer.parseInt()

``` java
def getLastNumber(str)
{
     int len = str.length();
     char c="";
     String s="";
     while(len>0){
         c = str[len-1];
         if("0123456789".contains(c+"")){
             s=c+s;
         }else{
             return Integer.parseInt(s);
         }
         len--;
     }
     return Integer.parseInt(s);
}
```

## getLastNumberWithSuffix

Returns the number in a string which is suffixed.
example :
getLastNumberWithSuffix("volume034storage","storage") 
	=> 34

Has dependencies with trimEnd & getLastNumber

``` java
def getLastNumberWithSuffix(text,suffix){
	return getLastNumber(trimEnd(text,suffix));
}
```


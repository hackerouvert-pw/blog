---
layout: post
title:  Obfuscation2
date:   2020-06-25
---
Write up for the Obfuscation 2 Challenge in the Web Client section of root me, link: https://www.root-me.org/en/Challenges/Web-Client/Javascript-Obfuscation-2

When we arrive on this Challenge we can only see a white background but there is more to it. When we inspect the anwer seems to be right in from of our eyes; there is a variable called 'pass'. Inside this variable the is the 'unescape()' function with a bunch of hexadecimal characters after. We try what we did in Obfuscation 1, to go on the cosole and type 'unescape(pass)'. This does return some usefull information but not the passwords exatly, we are only half way there.

We can see that what is returned is:
"unescape("String.fromCharCode(104,68,117,102,106,100,107,105,49,53,54)")"
The answer is in the numbers. Unfortunately we have to translate those numbers to letters as they all represent the Charcode of some letters.
One way of finding out what all these numbers are in letter is to create a simple code that does it for us:

    let numbers = String.fromCharCode(104,68,117,102,106,100,107,105,49,53,54)
    console.log(numbers)

What we are doing is storing all the characters in the variable 'numbers' which is going to transform them to characters
We then console.log numbers and we get our answer which is going to be the passcode for the Challenge.

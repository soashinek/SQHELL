This report documents my learning experience and practical work from the TryHackMe room titled SQhell.
- Objectives

The main objectives of this task were: to get better understanding about sql injuction

To understand what SQhell is

To learn how the attack works

To practice basic commands/tools

To answer all questions in the TryHackMe room

- What I Learned

From this task, I learned:

What SQ hell means

How attackers exploit vulnerabilities

Why input validation is important

Basic cybersecurity terminology

-Tools Used

The following tools were used during this task:

TryHackMe platform

Web browser

Terminal (Linux)
 



Task 1: find the flag error based sql

the aim  is login in to the data base to gain information

    -go to the login page and then write the user name and sqhell true statement 
         the statement that i used is =admin'AND 1=1#
         then i get the flag.

Task 2: time based sql

the spicia thing that we get in the process of finding the second flag To use union-based SQL injection to enumerate database tables and identify where sensitive data (the second flag) is stored within the database.

"sqlmap -u "http://10.10.218.134/" --headers="x-forward-for:1*" -dump " run this code on the terminal then we gat a lot of thins on it , we will get the flag after it finshes the process(running ).


Task 3: boolean based sql injuction 
the main objective of this task is To exploit a SQL injection vulnerability to enumerate the database tables and columns and extract the third flag from the vulnerable application.
 the code thyat i used to find the flag isb"sqlmap -"http://10.10.218.134/register/user -check?username =admin" -dump" use this code and pest on the terminal then you gonna get the flag.

Task 4:union  based (inception injuction)

 the main objective of finding this flag is to exploit a Boolean-based Blind SQL Injection  that is triggered through an HTTP Header, rather than a standard login form or URL parameter.

What makes this flag unique compared to others in the lab is its delivery method and the "blind" nature of the retrieval.
 -i think this task is a little complex than others.

Task 5:union based sql injunction

  we gat sql database  when we write tru statement 

  and we ganna find out how many column is exist in the database 
        writethe word  order by [the number of column---] -if we insert the wrong number of column it replays "unknown column'the noumber of column'in 'order clouse' "

       this is the code that i used to get the flag - "post?id=2 and 1=2 union select 1,2,concat(id,flag),4 from sqhell_5.flag LIMIT 0,1 --"



Challenge face
i got some challenges when -i am try to connect the vpn the problem was i removed the file and i was trying to coneect it, and i solved it by downloading the file and reconnect it .
       - the second challenge  that i get  is when i wrote the sqhell code i was suffered by spelling and spaces.
   -some times it was not working out even every things gose correctly. the solutions is try and try and try agan and agan then that  would be tyhe best solution.     

. Conclusion
 The SQHell challenge provides a comprehensive look at how SQL Injection  manifests in modern web applications. While many beginners assume SQLi only happens in login boxes, this lab proves that vulnerabilities can hide anywhere the application processes user input.

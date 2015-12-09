##Server Log Analysis

Full command

	grep date logname.log | awk '{print $1}' | sort -n | uniq -c | sort -rn | head

Breakdown

Retrieving a section of the log by date

	grep date logname.log

Count the number of IP addresses by calling the first column information 

	awk '{print $1}'
Where $1 calls the first column

Count the number of lines that have an occurence and sort

	sort -n

Get unique files and cut them down to a neat list

	uniq -c

Sort with the largest values first
	
	sort -rn

Print out the top results from the top of the file

	head
Leave this part off for the entire file


Material obtained from the following site:

	http://www.linuxjournal.com/article/7396

	and the cheat sheet from learn code the hard way
	
More

generating a log with just the known spiders/bots

	
	grep -i "spider\|bot" xalt-september.log > bots.log

generating a log without spiders/bots

	grep -v "spider\|bot" xalt-september.log > notbots.log

accumulating the number of times a bot accessed the site

	grep Sep/2015 bots.log | awk '{print $1}' | sort -n | uniq -c | sort -rn

Adding the date

	grep Sep/2015 bots.log | awk '{print $1,$4}' | sort -n | uniq -c | sort -rn


To look at in the future:
http://i-heart-geek.blogspot.com/2011/10/top-command-line-tips-apache-access-log.html
http://www.jafsoft.com/searchengines/webbots.html

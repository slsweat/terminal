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
material obtained from the following site:

	http://www.linuxjournal.com/article/7396

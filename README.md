Instructions

1. Hello fastping
--------------------------------------

to run a single experiments targeting google DNS server 8.8.8.8 pinging every 100ms during 1 second uploading all results to a local anonymous FTP:

	sudo ./fastpingBash/FastpingBash.py -t 8.8.8.8 -d 1 -f 0.1 -n 1 -R -C -S -Q -U 127.0.0.1 anonymous '' 21 up False

The same but getting local results (archive/hostname_unixtime.rw, stats/hostname_unixtime.st, .... customizable path for output, see point 4.)

	sudo ./fastpingBash/FastpingBash.py -t 8.8.8.8 -d 1 -f 0.1 -n 1 -R -C -S -Q 



2. More serious experiment
--------------------------------------

to run 10 experiments to ENST and google DNS /16 subnets pinging every 100ms for 24 hours (=288 blocs of 5 minutes), uploading only statistics every 5minutes to a local anonymous FTP, edit destination.txt so that it reads:

	137.194.0.0/24 
	8.8.0.0/16

then run:

	sudo ./fastpingBash/FastpingBash.py -t T destination.txt -d 300 -f 0.1 -1 -n 288 -S -U 127.0.0.1 anonymous '' 21 up False




3. Even more serious experiment
--------------------------------------

as above, reading destination list from destination.txt file (for very large detination sets)

	sudo ./fastpingBash/FastpingBash.py -T destination.txt -d 300 -f 0.1 -1 -n 288 -S -U 127.0.0.1 anonymous '' 21 up False



4. Even even more serious experiments
--------------------------------------

Read the helper for full customizability, helper:

	sudo ./fastpingBash/FastpingBash.py -h



This document is under construction.



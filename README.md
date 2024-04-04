Reads log files from tinydns and/or dnscache and prints them out in
human-readable form.  Logs can be supplied on stdin, or listed on
the command line:

    # cat @*.s | tinydnslog
    # tinydnslog -i @*.s
    # tail -f current | tinydnslog

Pipes each log file through tai64nlocal, which must be on your path.

Requirements:
 - tai64nlocal on the path
 - Python 3 or greater

Acknowledgments:

* The log format descriptions by Rob Mayoff were invaluable:
    http://dqd.com/~mayoff/notes/djbdns/tinydns-log.html
    http://dqd.com/~mayoff/notes/djbdns/dnscache-log.html

* Faried Nawaz's dnscache log parser was the original inspiration:
    http://www.hungry.com/~fn/dnscache-log.pl.txt

Written by Greg Ward <gward@python.net> 2001/12/13.

Modified to handle IPv6 addresses (as logged by djbdns with the patch at
http://www.fefe.de/dns/), 2003/05/03-04, prodded and tested by Jakob
Hirsch <jh@plonk.de>.

Modified to handle dnscache's AXFR request log lines by Malte Tancred
(http://tancred.com/malte.html), 2005/12/20.

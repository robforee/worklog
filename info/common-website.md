# Find most commonly used website
* download google history (last year)
	~/data/google-takeout
* extract and count the domains names
jq -c '.["Browser History"][1:] | .[] | [.time_usec, .url]' Takeout/Chrome/BrowserHistory.json | sed 's/.*\:\/\///' | sed 's/\/.*//' | sed 's/www\.//' >BrowserHistory.domains
sort BrowserHistory.domains | uniq -c | sort -n

## google queries
3565 queries / 137 = 26 queries per day

## cli notes 
4447 lines in 243 files / 137 = 33 lines per day
## notes in freemind
20,622 rows in 40 files / 137 = 150 lines per day


## manage notes in notion
1003 notion.so

## learning special
165 splunk
132 stackoveflow.com
126 nist.gov

## manage existing
188 datastudio.google.com
171 developers.google.com

## browser hits on github
1658 browser hits / 137 = 12 per day

#
1003 notion.so
498 reddit.com
188 datastudio.google.com
171 developers.google.com
165 splunk.com
132 stackoverflow.com
75 kali.org
67 nist.gov
59 nvd.nist.gov

## top 30 results over bootcamp ending Dec 10, 2021
cat ~/data/google-takeout/Takeout/Chrome/BrowserHistory.bootcamp

	192 days

   7429 docs.google.com = 38
   3565 google.com      = 19
   1921 newtab
   1658 github.com      = 9
   1471 mail.google.com
   1305 bootcampspot.com
   1205 drive.google.com  = 6
   1005 netflix.com
   1003 notion.so
    979 calendar.google.com
    498 reddit.com
    480 linkedin.com
    315 medicare.gov
    314 photos.google.com
    301 zoom.us
    240 amazon.com
    188 datastudio.google.com
    181 niccs.cisa.gov
    171 developers.google.com
    166 secure.ssa.gov
    157 publicstorage.com
    156 ercot.com
    147 docs.microsoft.com
    144 localhost
    132 stackoverflow.com
    118 kahoot.it
     97 192.168.1.254
     96 washingtonpost.com
     95 splunk.com
     91 youtube.com

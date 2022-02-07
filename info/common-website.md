# Find most commonly used website
* download google history (last year)
	~/data/google-takeout
* extract and count the domains names
jq -c '.["Browser History"][1:] | .[] | [.time_usec, .url]' Takeout/Chrome/BrowserHistory.json | sed 's/.*\:\/\///' | sed 's/\/.*//' | sed 's/www\.//' >BrowserHistory.domains
sort BrowserHistory.domains | uniq -c | sort -n

## top results

   9754 docs.google.com
   6078 google.com
   3257 newtab
   2673 mail.google.com
   2631 netflix.com
   2249 github.com
   1748 drive.google.com
   1627 notion.so
   1323 bootcampspot.com
   1032 calendar.google.com
    994 reddit.com
    658 linkedin.com
    613 indeed.com
    448 amazon.com
    396 scenariolab.com
    373 192.168.1.254
    325 medicare.gov
    323 photos.google.com
    319 capps.taleo.net
    311 datastudio.google.com
    305 zoom.us
    234 stackoverflow.com
    226 docs.microsoft.com
    208 developers.google.com
    202 niccs.cisa.gov
    196 washingtonpost.com
    192 ercot.com
    182 youtube.com
    172 publicstorage.com
    166 secure.ssa.gov

# Domainker (Beta)
My personal bugbounty tool

# How to use
I developed this tool to be easily managed and upgraded so i created it as small plugin systems connected together

## Plugins and usage
```
lib\modules\aws.py   : [--aws] Checks if the host is regirested on amazon (Can be useful in Sub-domain TakerOver)
lib\modules\cname.py : [--dns] Returns the host cname
lib\modules\url.py   : [--url] Returns host response code
```

## Basic usage
 ```
 $ python domainker.py -d mydomains_list.txt [.. Plugins]
 $ python domainker.py -d mydomains_list.txt --url
 $ python domainker.py -d mydomains_list.txt --dns
 $ python domainker.py -d mydomains_list.txt --aws
 ```
You could also use multiple plugins at the same time
```
$ python domainker.py -d mydomains_list.txt --url --dns --aws
```
## Options
```
$ python domainker --help
```
- Create output file [--output/-o file_name]
- Threads count [--threads/-t number]
- Takeover aws [--aws-takeover/-x] Add your AWS account creds at `lib\modules\aws.py`
- Thread timeout [--thread-timeout/-T seconds]
- Request timeout [--request-timeout/-rt seconds]


# Format 
I want add different formats at the future but currenlty this tool only support this format for the domains file
```
https://sub.domain.com  
http://sub.domain.com  
sub.domain.com  
.sub.domain.com
```
Which generated by:
- amass  
- aquatone (hosts.txt)  
- subfinder  
- sublist3r  
... and many other subdomain finders  

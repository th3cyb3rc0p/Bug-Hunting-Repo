# Bug Bounty Hunting:

I prefer below available resources to succeed in Bug Bounty Hunting. I'll update this monthly with new techniques. Some of my bug bounty disclosures are available in http://nullnews.in


## Platforms:


1. OpenBugBounty - (XSS/CSRF/IDOR)(Will accept report from any site)
2. BugCrowd
3. HackerOne
3. Cobalt.io
4. SynAck (Only invited researchers)
5. Other self hosted programs by different domains (Facebook Whitehat/Google VRP/ AT&T BB)

## Sub Domain Enumeration:


1. Enumall
2. Massdns
3. Sublist3r
4. Knock
5. VirusTotal
6. Shodan
7. Censys
8. Eye witness
9. DNS Dumpster (https://dnsdumpster.com)
10. Google Dorking (site:sony.com -www)
11. Virus Total
12. https://github.com/appsecco/bugcrowd-levelup-subdomain-enumeration
13. DNSScan
14. Altdns
15. dns-parallel-prober
16. brutesubs
17. dirsearch
18. Aquatone

## Sub Domain Takeovers:


### Cloudfront Entries

``` 
 ride.uber.com -  cname - cloudfront.com
 xxxx.ubnt.com - cname - cloudfront.com
```
### AWS Misconfiguration

```
 rubyci.s3.amazonaws.com
 hackerone
 uber
 ubiquitinetworks
 twitter etc.
```
### Default Pre-Installed Instances (Install-Update Credentials-Report)

> snapchat wordpress instance - blog.bitstripsforschools.com (https://hackerone.com/reports/274336)

### Unbouncepages

``` Cname: unbouncepages.com
 Name: landing.udemy.com
 Type: CNAME
 Class: IN
 TTL: 300
```
### Google Mapped Domains

```
216.58.203.243    moderator.ubnt.com
216.58.203.243    ghs.google.com
216.58.203.243    ghs.l.google.com
```
## Automation:

1. autoSubTakeover [Github]
2. HostileSubBruteforcer
3. tko-subs


## Git - Recon:

1. gitrob
2. git-all-secrets
3. trufflehog
4. git-secrets
5. repo-supervisor

## API Enumeration from JS files:

> https://github.com/GerbenJavado/LinkFinder


## Acquisition Enumeration:

1. Crunchbase
2. https://crt.sh
3. https://censys.io
4. https://google.com/transparencyreport/https/ct

## Content Discovery / Dir Bruting:

1. Wappalyzer
2. Retire.js [Burp]
3. Built With
4. Vulners CVE Scanner [Burp]
5. Patator
6. GoBuster
7. WPScan
8. CMSMap
9. Robots Disallowed [GitHub By DanielMiessler]
10.Burp Content Discovery
11.CMSExplorer
12.BlindElephant

## Content Management System Bugs:

```
Adobe Cold Fusion - (Famous RCE/Admin Salt Leakage/SQL Vuln)
Drupal CMS - (RCE)
Wordpress - (Plenty of Bugs)
Jenkins Automation Server
```
## Parameter Bruter:


1. Parameth
2. Back Slash Powered Scanner [Burp]

## XSS:


1. Polyglot
2. Flash - https://cure53.de/flashbang
3. Common Input Vectors
4. Blind XSS Frameworks
	- Sleepy Puppy [Python]
	- XSS Hunter [Python]
	- Ground Control [Ruby/Smail]
5. XSS MindMap [https://github.com/jackmasa/]
6. XSS Hunter
7. Flash XSS (FFDec-ompiler, https://github.com/riusksk/FlashScanner, https://cure53.de/flashbang)

## Flash CSRF:

1. Target is Accepting on JSON format data and Blocking Cross Domain requests with CORS.

> https://www.geekboy.ninja/blog/tag/flash-csrf/

## SSTI:


1. TPLMap + TPLMap [Burp Extension]

## SSRF:

```
Blind SSRF - Google PoC.
		   - Twitter PoC.
		   - AWS metadata acquiring
Full SSRF

Out of Band
```
## OAuth/OpenRedirect:


> Validation missing on State/Token/Code (Open Redirection on Google Acquisition)

## Fuzzing API:


> Fuzzapi https://github.com/Fuzzapi/fuzzapi

## Logical Bugs:

```
Email Verification Check fails

Money Rounding Issues.
```
## Denial of Service:

```
Via Large input.

Via Images.

Via XLS/PDF/TXT.

Via Out of Band Blind SSRF.
```
## Android-Hunts:
```
Decompile app --> Look for /assets/  or /res/raw [AWS Prod Keys, Dev Leftovers]
Check for External Storage - Binary Info/Code without validation, Sandbox leak, GPS Info, Log Files
Detecting Read/Write External Storage - FileObserver
Obfuscation - Proguard
Webview Checks -
				-> setAllowContent
				-> setAllowFileAccess
				-> setAllowFileAccessFromURLs
				-> setJavaScriptEnabled
				-> setPluginState
				-> setSavePassword  
JavaScriptInterfaces - "jsvar"   -------> RCE CVE-2012-6636 (SDK<=17 supported apps vulnerable)
```
## Payloads:

1. https://github.com/1N3
2. https://github.com/danielmiessler/SecLists

## Ref:

> https://github.com/ngalongc/bug-bounty-reference

> bugbounty.community/tools


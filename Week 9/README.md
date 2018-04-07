# Project 9 - Honeypot

Time spent: **6** hours spent in total

> Objective: Setup a honeypot and intercept some attempted attacks in the wild.

## Summary

We used the well-supported open source honeypot [Modern Honey Network](https://github.com/threatstream/mhn) deployed through [Google Compute Platform](https://cloud.google.com/) as our setup. We created an `mhn-admin` and four other `mhn-honeypot` VM instances on [Google Compute Engine](https://cloud.google.com/compute/).

![Imgur](https://imgur.com/V3jo2Dr.png)

We deployed these four honeypots to each of the `mhn-honeypot` VMs:

1. `mhn-honeypot-1` - [Dionaea over HTTP](https://github.com/rep/dionaea)
2. `mhn-honeypot-2` - [Wordpot](https://github.com/threatstream/wordpot)
3. `mhn-honeypot-3` - [Elastichoney](https://github.com/threatstream/elastichoney)
4. `mhn-honeypot-4` - [Snort](https://github.com/threatstream/snort)

After about a week of data collection, there were **~40,000** attacks on the Dionaea over HTTP honeypot, **~2,000** attacks on the Snort honeypot, and **~10** attacks on the Elastichoney honeypot. There were **0** attacks on the Wordpot honeypot.

> NOTE: The Snort honeypot was started mid-week and had around half the time to collect data.

![Imgur](https://imgur.com/nAXsQzy.png)

## Details

These were the specific VM instances deployed through Google Compute Engine along with their corresponding honeypots and attack counts.

Name             | Zone       | Internal IP | External IP | Start | End | Honeypot | Attacks
---------------- | :--------: | :---------: | :---------  | ----- | --- | -------- | -------
`mhn-admin`      | us-west1-a | 10.138.0.2  | [35.185.201.249](http://35.185.201.249) | Apr 1, 2018 9:02 PM  | Apr 7, 2018 6:14 PM | *N/A*    | *N/A*
`mhn-honeypot-1` | us-west1-a | 10.138.0.3  | [35.185.220.57](http://35.185.220.57)   | Apr 1, 2018 10:10 PM | Apr 7, 2018 6:14 PM | [Dionaea over HTTP](https://github.com/rep/dionaea) | **39856**
`mhn-honeypot-2` | us-west1-a | 10.138.0.4  | [35.185.212.44](http://35.185.212.44)   | Apr 1, 2018 10:58 PM | Apr 7, 2018 6:14 PM | [Wordpot](https://github.com/threatstream/wordpot) | **0**
`mhn-honeypot-3` | us-west1-a | 10.138.0.5  | [35.197.37.232](http://35.197.37.232)   | Apr 1, 2018 11:00 PM | Apr 7, 2018 6:14 PM | [Elastichoney](https://github.com/threatstream/elastichoney) | **12**
`mhn-honeypot-4` | us-west1-a | 10.138.0.6  | [35.227.155.38](http://35.227.155.38)   | Apr 4, 2018 8:43 PM  | Apr 7, 2018 6:14 PM | [Snort](https://github.com/threatstream/snort) | **1845**

### Statistics

#### Top 5 Attacker IP addresses (24 hrs.)

|   | Country     | Flag  | IP address | Count
|---| ----------- | :---: | :--------- | ----:
| 1 | *N/A*       | *N/A* | [5.62.39.232](http://35.185.201.249/ui/attacks/?source_ip=5.62.39.232)     | 316
| 2 | Russia      | <img src=http://flags.fmcdn.net/data/flags/w1160/ru.png height=24 /> | [5.188.11.145](http://35.185.201.249/ui/attacks/?source_ip=5.188.11.145)   | 307
| 3 | China       | <img src=http://flags.fmcdn.net/data/flags/w1160/cn.png height=24 /> | [101.236.25.53](http://35.185.201.249/ui/attacks/?source_ip=101.236.25.53) | 104
| 4 | Netherlands | <img src=http://flags.fmcdn.net/data/flags/w1160/nl.png height=24 /> | [185.56.81.51](http://35.185.201.249/ui/attacks/?source_ip=185.56.81.51)   | 88
| 5 | Ukraine     | <img src=http://flags.fmcdn.net/data/flags/w1160/ua.png height=24 /> | [193.106.31.34](http://35.185.201.249/ui/attacks/?source_ip=193.106.31.34) | 76

#### Top 5 Attack Signatures (24 hrs.)

|   | Attack Signature                                                   | Count
|---| ------------------------------------------------------------------ | ----:
| 1 | ET DROP Dshield Block Listed Source group 1                        | 229
| 2 | ET CINS Active Threat Intelligence Poor Reputation IP TCP group 4  | 65
| 3 | ET CINS Active Threat Intelligence Poor Reputation IP TCP group 65 | 49
| 4 | ET SCAN Sipvicious User-Agent Detected (friendly-scanner)          | 22
| 5 | ET SCAN Sipvicious Scan                                            | 15

## Problems

The Wordpot honeypot was the only one that didn't show any attacks, despite efforts of running `nmap` and `wpscan` against the honeypot.

```
root@kali:~# wpscan --url http://35.185.212.44 --random-agent
_______________________________________________________________
        __          _______   _____                  
        \ \        / /  __ \ / ____|                 
         \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
          \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \ 
           \  /\  /  | |     ____) | (__| (_| | | | |
            \/  \/   |_|    |_____/ \___|\__,_|_| |_|

        WordPress Security Scanner by the WPScan Team 
                       Version 2.9.3
          Sponsored by Sucuri - https://sucuri.net
   @_WPScan_, @ethicalhack3r, @erwan_lr, pvdl, @_FireFart_
_______________________________________________________________


[!] The WordPress URL supplied 'http://35.185.212.44/' seems to be down. Maybe the site is blocking wpscan so you can try the --random-agent parameter.
```

## Notes

The MHN honeypots were easy to set up. After starting the VM instances on Google Compute Engine, it was simply a matter of running the commands for each honeypot provided in the MHN admin console. Setting up Google Compute Engine was much more involved.

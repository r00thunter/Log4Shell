<h1 align="center">log4shell</h1>
<h4 align="center">A fully automated, accurate, and extensive scanner for finding vulnerable log4j hosts</h4>

# Features

- Support for lists of URLs.
- Fuzzing for more than 60 HTTP request headers.
- Fuzzing for HTTP POST Data parameters.
- Fuzzing for JSON data parameters.
- Supports DNS callback for vulnerability discovery and validation.
- WAF Bypass payloads.

---
# Announcement

There is a patch bypass on Log4J v2.15.0 that allows a full RCE. This log4j-scan script reliably detect CVE-2021-45046. If you're having difficulty discovering and scanning your infrastructure at scale or keeping up with the Log4J threat.


# Description

This script shall be used by security teams to scan their infrastructure for Log4J RCE, and also test for WAF bypasses that can result in achiving code execution on the organization's environment.

It supports DNS OOB callbacks out of the box, there is no need to setup a DNS callback server.


# Installation

```
$ git clone 
$ pip3 install -r requirements.txt

```
# Usage

## Scan a Single URL

```
$ python3 log4shell.py -u <target url>
```

## Scan a Single URL using all Request Methods: GET, POST (url-encoded form), POST (JSON body)


```
$ python3 log4shell.py -u <target url> --run-all-tests
```

## Discover WAF bypasses on the environment.

```
$ python3 log4shell.py -u <target url> --waf-bypass
```

## Scan a list of URLs

```
$ python3 log4shell.py -l url-list.txt
```

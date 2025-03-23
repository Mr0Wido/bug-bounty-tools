# Bug Bounty Tools

Most of the tools include a one-liner bash command. I use them in Python.

### SSTI Scan

```bash
$ python3 sstiscan.py -ul urls.txt
```

### CORS Scan

__cors.py__ include one-liner commands. For these;
- Basic Origin Reflection
- Trusted null Origin payload
- Whitelisted null origin value payload
- Trusted subdomain in Origin payload
- Abuse on not properly Domain validation
- Origin domain extension not validated vulnerability payload

```bash
$ python3 cors.py -ul urls.txt -d example.com
```

__[corscan.py](https://github.com/AngixBlack/Corscan/tree/main)__   belongs [AngixBlack](https://github.com/AngixBlack). I use this tool for one of my projects, and it does not include a silent option, so I added some codes. 
- print(logo) Turn in to comment.
- I added this fıntion __remove_ansi_escape_sequences__ for clean output.

### CSRF Scan

The tool includes a one-liner bash command.
```bash
$ python3 csrfscan.py -ul urls.txt 
```

### LFI Scan

The tool includes a one-liner bash command. And needs a payload.

```bash
$ python3 lfiscan.pt -l urls.txt -p wordlist/lfipayload.txt
```

### Open Redirect Scan

This tool belongs to [devanshbatham](https://github.com/devanshbatham). I just clear colors, and banners, and for plain results.
```bash
$ cat urls.txt | python3 redirectscan -p wordlist/redirect_payloads.txt -k FUZZ 
```

### SSRF Scan

SSRFIRE - This tool belongs to [ksharinarayanan](https://github.com/ksharinarayanan). Tool is a bash script so I turned to the python. And I delete the colors and banners. Because I need plain results, and just scan ssrf.

```bash
$ python3 ssrfscan -f urls.txt -s {server}
```

# Scenario: Saint John: what is writing to this log file?
Level: Easy
```bash
  kill -9 $(ps aux | grep bad.log | grep -v grep | awk '{print $2}') 
```

# Scenario: "Saskatoon": counting IPs.
Level: Easy
```bash 
  awk '{print $1}' access.log | sort | uniq -c | sort | tail -n 1 | awk '{print $2}' > /home/admin/highestip.txt
```

# Scenario: "Taipei": Come a-knocking
Level: Easy

```bash 
  nmap -p- localhost
```

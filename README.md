# Scenario: Saint John: what is writing to this log file?
Level: Easy
```bash
  PID=$(ps aux | grep bad.log | grep -v grep | awk '{print $2}'); kill -9 $PID 
```

# Scenario: "Saskatoon": counting IPs.
Level: Easy

```bash 
  cat access.log | awk '{print $1}' | sort | uniq -c | sort | tail -n 1 | awk '{print $2}' > /home/admin/highestip.txt
```

# Scenario: "Taipei": Come a-knocking
Level: Easy

```bash 
  nmap -p- localhost
```

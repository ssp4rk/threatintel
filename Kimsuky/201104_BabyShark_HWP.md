# Brief description
|Actor|Cluster|Description|
|--|--|--|
|Kimsuky|BabyShark|Malicious HWP file disguised as the USA 2020 election prediction|

# Malware Information
|Hash|File name|ITW|
|----------------------------------------------------------------|--------------------------------|--|
|3fb0cfe3cc84fc9bb54c894e05ebbb92|미국 대선 예측 - 미주중앙일보.hwp||
|96a0a69c8ce18c1402b70cec472a9782|%appdata%\\Microsoft\Amazon.xml|hxxp://xeoskin.co[.]kr/wp/wp-includes/SimplePie/Net/cross.php?op=1|
|d5e8eb9d271f2621605764da2ac86f1c|suf.hta|hxxp://xeoskin.co.kr/wp/wp-includes/SimplePie/Net/suf.hta|
|0a9de266423f3ff197fbd3ec9187dc0d|N/A|hxxp://xeoskin.co.kr/wp/wp-includes/SimplePie/Net/cross.php?op=3|
|b11ca13625dd0980e7cab1a86293f1a2|N/A|hxxp://xeoskin.co[.]kr/wp/wp-includes/SimplePie/Net/cross.php?op=2|

# Network Indicators
hxxp://xeoskin.co[.]kr/wp/wp-includes/SimplePie/Net/cross.php?op=1  
hxxp://xeoskin.co[.]kr/wp/wp-includes/SimplePie/Net/suf.hta  
hxxp://xeoskin.co[.]kr/wp/wp-includes/SimplePie/Net/cross.php?op=3  
hxxp://xeoskin.co[.]kr/wp/wp-includes/SimplePie/Net/cross.php?op=2  
boundary: ----1f341c23b5204

# Host Indicators
## File path
|File path|Description|
|----------------------------------------------------------------|--------------------------------|
|%appdata%\Microsoft\Office\version.xml | fetched suf.hta|  
|%appdata%\Microsoft\Network\sr011.xml |Victim information, Keylogging|  
|%appdata%\Microsoft\Network\conv.xml | Encoded host profile|  
|%appdata%\Microsoft\Amazon.xml | fetched file|

## Mutex name
Global\AlreadyRunning191122

## Schedule Task name
AhnlabUpdate

# MITRE ATT&CK
|Tactics|Techniques|
|-----|----|
|Initial Access|T1566.001 Phishing: Spearphishing Attachment |
|Execution|T1059.001 Command and Scripting Interpreter: PowerShell|
|         |T1059.005 Command and Scripting Interpreter: Visual Basic|
||T1053.005 Scheduled Task/Job: Scheduled Task|
|Persistence|T1053.005 Scheduled Task/Job: Scheduled Task|
|Privilege Escalation||
|Defense Evasion|T1140 Deobfuscate/Decode Files or Information|
|Credential Access||
|Discovery||
|Lateral Movement||
|Collection|T1056.001  Input Capture: Keylogging|
|Command and Control|T1132.001  Data Encoding: Standard Encoding|
||T1071.001 Application Layer Protocol: Web Protocols|
|Exfiltration|T1041 Exfiltration Over C2 Channel|
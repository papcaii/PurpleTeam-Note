# Defense Evasion

Defense Evasion refers to tactics used by attackers to avoid detection and bypass security measures during their cyberattacks.
There are some of attackers behaviors:
- hide attacker (payload, malware, ...) activities
- avoid triggering security alerts
- evade the detection of their malicious actions

In this context, I will cover some techniques that I think is effective !

## AV Bypass

### Why 
Obviously in the client's system always have protection, one of those is Anti-Virus, like:
- Kaspersky Antivirus
- Bitdefender Antivirus
- Windows Defender
- ...

So if we can bypass these it would be easier for us to do malicious things

### Mechanism
Yeah, reverse :)) The first step when exploit is understand how our target work.  
As I know most AV at the moment work by 2 main mechanism:
- Static Analysis
  - Signature-Based Detection:

    - Hashing: The AV calculates a cryptographic hash (e.g., MD5, SHA-1, SHA-256) of the entire file or specific sections of the file. This hash acts as a unique fingerprint.

    - Signature Matching: The calculated hash is compared against a database of known malware signatures. If a match is found, the file is flagged as malicious.

  - Heuristic Analysis:

    - Generic Signatures: AVs use generic signatures that identify common patterns or code structures often found in malware, even if the exact code sequence is not in the database.

    - Rule-Based Analysis: AVs apply a set of rules to analyze the file's characteristics and behavior. These rules are based on common malicious patterns, such as attempts to modify system files, inject code into other processes, or establish network connections to known command and control servers.

- Dynamic Analysis

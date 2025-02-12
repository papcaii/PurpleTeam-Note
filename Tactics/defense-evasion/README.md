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
  - Behavioral Monitoring:

    - System Call Monitoring: The sandbox monitors the system calls (interactions with the operating system kernel) made by the running file. This can reveal actions like creating or modifying files, accessing the registry, starting processes, and making network connections.

    - API Hooking: The sandbox may hook (intercept) API calls made by the file to observe its interactions with system libraries and other applications. This provides more detailed information about the file's behavior.

    - Process Monitoring: The sandbox tracks all processes created or manipulated by the file, including their memory usage, resource consumption, and interactions with other processes.

    - Network Monitoring: The sandbox monitors all network traffic generated by the file, including DNS requests, HTTP/HTTPS connections, and other protocol interactions. This can reveal attempts to communicate with command and control servers, download additional malware, or exfiltrate data.

    - File System Monitoring: The sandbox monitors all file system activity, including file creation, deletion, modification, and access.

    - Registry Monitoring: The sandbox monitors changes made to the Windows Registry.

### Method
So now we know 2 main mechanisms that AV use, so the method should be splitted into 2 categories

#### Static Analysis
This I think this is not as hard as the dynamic one, and here is some ways:
- Encode Payload
- Steganography

#### Dynamic Analysis
- Disable AV:
  - [NullAmsi]: A payload that disable amsi.dll (a dll that support AV in dynamic analysis)

# PurpleTeam-Note

I write this for knowledge I have learnt for purple team

## Privilege Escalation

## Lateral Movement

### PsExec
Attackers often use PsExec to perform lateral movement from one endpoint to another
It's important to note that there are different flavors of PsExec. For example: 
- SysInternals PsExec (The official one).
- Impacket PsExec (Part of impacket suite).
- Metasploit, CobaltStrike, or Empire PsExec (Any C2 framework basically)

#### How it work
PsExec work primary on SMB protocol (often by port 445). When we use

```powershell
.\PsExec64.exe \\#{remote.computer.ip} -u #{domain.admin.username} -p #{domain.admin.password} -i whoami
```

PsExec will deploy PsExecsvc (by default) on the endpoint. This service will execute command and return output to us

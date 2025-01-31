# DLL Side-Loading
This is a method that leverage DLL search mechanism of Windows when an application load DLL

## DLL search order
1. The directory from which the application loaded.
2. Custom search paths (provided by the user).
3. The system directory (e.g., C:\Windows\System32).
4. The Windows directory (e.g., C:\Windows).
5. The current directory.
6. Directories that are listed in the PATH environment variable.

## Reference

### POCs/Experience

- **[Red, Blue, Purple Team in DLL Sideloading](https://www.cybereason.com/blog/threat-analysis-report-dll-side-loading-widely-abused):** Worth to read this

#### Red Team
- **[Evading EDR by DLL Sideloading in C#](https://globetech.biz/index.php/2023/05/19/evading-edr-by-dll-sideloading-in-csharp/)**

#### Blue Team

### Known Vulnerable DLLs

- **[Up-to-Date List of Vulnerable DLLs](https://hijacklibs.net/)**

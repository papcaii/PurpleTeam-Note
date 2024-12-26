# DLL Side-Loading
This is a method that leverage DLL search mechanism of Windows when an application load DLL

## DLL search order
1. The directory from which the application loaded.
2. Custom search paths (provided by the user).
3. The system directory (e.g., C:\Windows\System32).
4. The Windows directory (e.g., C:\Windows).
5. The current directory.
6. Directories that are listed in the PATH environment variable.

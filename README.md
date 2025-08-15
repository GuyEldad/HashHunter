<p align="center">
  <img src="HashHunter.jpg" alt="HashHunter Banner" width="700">
</p>

# HashHunter

**HashHunter** is a forensic tool for scanning files that match a specific hash on Windows 2000, XP, 7, and newer version systems.
It was built for environments where tools like PowerShell, certutil, other modern utilities, or third-party tools are unavailable or incompatible.
The tool enables scanning of a specific path or a full search across all existing drives, including hidden locations, to identify potentially suspicious files.
It is built to streamline the investigation process and quickly identify the hash, saving valuable time during security incident investigations and threat hunting.

## Features
- Compatible with **Windows 2000, XP, 7**, and all modern Windows systems (x86/x64).
- Supports scanning a **specific file or folder** (folders are scanned recursively) or performing a **full-drive search** across all available drives.
- Performs hash lookups using **MD5**, **SHA1**, or **SHA256**.
- Provides a **delete or skip** prompt after matches are found.
- `<Path>` may point to a single file or a folder.

**Note:** Some protected directories (e.g., `C:\Windows\System32`) require administrative privileges to delete files.

## Usage
```
HashHunter.exe -MD5    <Hash> -Path <Path>
HashHunter.exe -SHA1   <Hash> -Path <Path>
HashHunter.exe -SHA256 <Hash> -Path <Path>

HashHunter.exe -MD5    <Hash> -Fullscan
HashHunter.exe -SHA1   <Hash> -Fullscan
HashHunter.exe -SHA256 <Hash> -Fullscan
```

## Examples
```
HashHunter.exe -SHA1 50b526b85911b9e0dc9d4ddd2879f09ca36bdf6a -Path C:\Users\<User>\Desktop
HashHunter.exe -MD5  64F63DCDD0AF4CD6A0B74E7FF128F207 -Fullscan
```

## Important Notice

Some antivirus software may flag the executable version of this tool as a false positive.  
This can occur due to the nature of the tool's functionality (file scanning and deletion) and the way it is compiled as a standalone executable.

If you encounter warnings, please consider the following:
- Running the tool in a sandbox or virtual machine.
- Adding an exclusion rule for the executable in your antivirus software.
- Temporarily disabling your antivirus software while running the scan.

## Contact

For questions or feedback, please contact me via:  
https://www.linkedin.com/in/guy-eldad/

© 2025 Guy Eldad. All rights reserved.

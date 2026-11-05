# Project Collection

Project Collection is a local desktop app for Windows and Linux that turns the
history of a project built with AI coding assistants into a **development
history** (how it was actually built) and a **build guide** that someone else
can follow to rebuild it from zero, also without AI. Everything stays on your
computer; no account is needed.

## Download

| System | Download |
|---|---|
| Windows 10/11 (x64) | [Project-Collection-Setup.exe](https://github.com/Emea123/project-collection-releases/releases/latest/download/Project-Collection-Setup.exe) |
| Linux (x64), AppImage | [Project-Collection-x86_64.AppImage](https://github.com/Emea123/project-collection-releases/releases/latest/download/Project-Collection-x86_64.AppImage) |
| Debian / Ubuntu (x64), .deb | [project-collection_amd64.deb](https://github.com/Emea123/project-collection-releases/releases/latest/download/project-collection_amd64.deb) |

The links always point to the newest release. Release notes, older versions
and `SHA256SUMS.txt` (checksums of every file) are on the
[releases page](https://github.com/Emea123/project-collection-releases/releases).

## Install

- **Windows:** run `Project-Collection-Setup.exe`. It installs for your Windows
  account only, without administrator rights, and adds Start menu and desktop
  shortcuts.
- **AppImage:** make it executable and start it:
  `chmod +x Project-Collection-x86_64.AppImage && ./Project-Collection-x86_64.AppImage`
- **Debian / Ubuntu:** `sudo apt install ./project-collection_amd64.deb`, then
  start *Project Collection* from the app menu or with `project-collection`.

**Git** must be installed (Windows: `winget install --id Git.Git -e`, Debian /
Ubuntu: `sudo apt install git`). On the first start, a setup guide checks Git
and offers the optional tools.
Project Collection tells you about new versions and opens the releases page;
you download and run the new installer yourself. Your projects and settings
are kept.

### Warnings from Windows and security software

Project Collection does not carry a digital signature yet, so Windows and security
software do not know the publisher. AVG, Avast, Microsoft Defender SmartScreen or
other security software may show a warning or check the file before it runs. Such a
warning does not by itself mean that malware was found, but take it seriously.

1. **Download only from the
   [releases page](https://github.com/Emea123/project-collection-releases/releases)**
   and compare the file with `SHA256SUMS.txt` there (Windows PowerShell:
   `Get-FileHash <file> -Algorithm SHA256`, Linux: `sha256sum --check --ignore-missing
   SHA256SUMS.txt`). A matching checksum shows that the file is complete and is the one
   published there. It does not replace a code signature.
2. **If your security software checks the file, wait for the check.** AVG and Avast,
   for example, may show "Suspicious file detected" (CyberCapture) once for each new
   file: the installer, the program on its first start and, if you install it,
   SkillSpector. Close the message without choosing an option such as "Open anyway".
   According to AVG the check usually takes up to a few hours, but it can take longer,
   and we cannot promise a fixed time.
3. **If a threat is reported or the file is moved to quarantine, stop.** Do not run
   the file, and report the finding in the
   [issues of this repository](https://github.com/Emea123/project-collection-releases/issues)
   with the name of your security software and its message.
4. **If you believe it is a false positive**, use the official false-positive or
   support form of your security software's vendor.

Do not turn off your security software, do not add an exception and do not override a
threat warning.

**Windows SmartScreen** may show "Windows protected your PC" because this app is not
code-signed yet, so the publisher is unknown to Microsoft. This is not a report that
malware was found. If you downloaded the file from the releases page and its SHA-256
matches `SHA256SUMS.txt`, you can continue: choose **More info** and then **Run anyway**.
Only do this for a file whose checksum you have verified. This is different from a virus
scanner reporting an actual threat: if that happens, stop and do not run the file.

In our test of version 1.1.2 on Windows 11 with AVG active, AVG CyberCapture first held
the installer and sent it to AVG's lab. Later the same installer started without a new
warning, and installing it and keeping existing data were checked successfully. AVG
did not show us a result of its lab analysis. Only AVG was tested.

## License

Project Collection is proprietary software, free to download and use; see
[LICENSE](LICENSE). It is not open source, and this repository contains only
releases, no source code. Third-party components are listed in
`THIRD-PARTY-NOTICES.txt` in the installed application folder.

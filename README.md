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
and offers the optional tools. Later versions can be installed from
Settings → Updates inside the app; your projects and settings are kept.

### Windows SmartScreen

The installer is not code-signed yet, so Windows may show "Windows protected
your PC". Make sure the file came from this page, then choose
**More info → Run anyway**. Right after installing, your virus scanner may
check the new program for a few seconds before it opens the first time.

## License

Project Collection is proprietary software, free to download and use; see
[LICENSE](LICENSE). It is not open source, and this repository contains only
releases, no source code. Third-party components are listed in
`THIRD-PARTY-NOTICES.txt` in the installed application folder.

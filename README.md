# Ladybird Windows Autobuilds

[![Build win32 (.exe)](https://github.com/Elwynsiaa/ladybird-windows-autobuild/actions/workflows/build-win32.yml/badge.svg)](https://github.com/Elwynsiaa/ladybird-windows-autobuild/actions)
[![Latest Release](https://img.shields.io/github/v/release/Elwynsiaa/ladybird-windows-autobuild?include_prereleases&color=blue&label=latest%20build)](https://github.com/Elwynsiaa/ladybird-windows-autobuild/releases)
[![Web Directory](https://img.shields.io/badge/Website-GitHub%20Pages-181717?logo=github&logoColor=white)](https://elwynsiaa.github.io/ladybird-windows-autobuild/)
[![Upstream](https://img.shields.io/badge/Upstream-LadybirdBrowser%2Fladybird-ff69b4)](https://github.com/LadybirdBrowser/ladybird)

Unofficial repository providing **automated native Windows (`x86_64`) binaries** for the [Ladybird](https://github.com/LadybirdBrowser/ladybird) web browser. 

These builds are compiled directly from the upstream `master` branch using GitHub Actions on a weekly schedule.

🌐 **Browse and download builds online:** [https://elwynsiaa.github.io/ladybird-windows-autobuild/](https://elwynsiaa.github.io/ladybird-windows-autobuild/)

---

> [!WARNING]
> **Experimental Builds:** Native Windows support in Ladybird is in early and active development. These builds track the bleeding-edge upstream `master` branch. **Most builds are expected to be unstable, incomplete, or may crash unexpectedly.** Use strictly for testing and experimentation.

---

## ⬇️ Downloads

You can download the packaged `.zip` builds directly via:
* **Web UI:** [elwynsiaa.github.io/ladybird-windows-autobuild](https://elwynsiaa.github.io/ladybird-windows-autobuild/)
* **GitHub Releases:** **[Releases](../../releases)** page

### Build Details
* **Cadence:** Weekly automated builds (Every Sunday at 00:00 UTC) + manual trigger on demand.
* **Artifact:** `Ladybird-Windows-Release.zip` (contains the browser binary and bundled runtime DLLs / Qt plugins).

---

## 🚀 Getting Started

1. Download `Ladybird-Windows-Release.zip` from the [Web Directory](https://elwynsiaa.github.io/ladybird-windows-autobuild/) or [Releases](../../releases).
2. Extract the `.zip` archive to a folder on your PC.
3. Open the extracted folder and launch `bin/Ladybird.exe`.

---

## 🛠️ How It Works

The workflow automatically compiles the browser directly from source using GitHub Actions:

- **Source:** Checked out directly from [`LadybirdBrowser/ladybird`](https://github.com/LadybirdBrowser/ladybird) (`master` branch).
- **Environment:** `windows-latest` with `ClangCL` toolchain and CMake.
- **Dependency Management:** Managed via `vcpkg` and pre-cached binaries.
- **Post-processing & Bundling:** Automatically locates and packages necessary Qt platform plugins (`platforms/qwindows.dll`), image formats (`imageformats/`), helper executables, and required runtime `.dll` libraries into a standalone distribution ZIP.

---

## ⚖️ Disclaimer

This is an **unofficial community project** and is **not affiliated with, endorsed by, or maintained by the Ladybird Browser project or its core developers**. 

* For bug reports and issues with the official browser, visit the official repository: [LadybirdBrowser/ladybird](https://github.com/LadybirdBrowser/ladybird).
* Please do not submit bug reports to upstream regarding broken Windows builds unless you are actively contributing to native Windows support fixes.

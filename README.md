# PortLark Scoop bucket

Install the [PortLark](https://portlark.com/) desktop client for sharing local apps through HTTPS tunnels on Windows 10 or 11 (64-bit).

This is a standalone product bucket. It is not part of Scoop's Main or Extras buckets. The manifest downloads the versioned ZIP directly from portlark.com and verifies its SHA-256 checksum; this repository does not redistribute binaries.

## Install

Install [Scoop](https://scoop.sh/) and Git first, then run in PowerShell:

```powershell
scoop bucket add portlark https://github.com/qiyadeng/scoop-portlark
scoop install portlark/portlark-desktop
```

Open **PortLark** from the Start menu. This GUI package does not create a `portlark` command-line shim. A PortLark account is required to connect a tunnel. See the [website](https://portlark.com/) and [terms](https://portlark.com/terms) for current trial and subscription details.

## Update and uninstall

```powershell
scoop update
scoop update portlark-desktop
# To remove the application:
scoop uninstall portlark-desktop
# Optional: remove this bucket afterwards:
scoop bucket rm portlark
```

Decline in-app updates for this installation so that Scoop's recorded version stays accurate. Updates become available only after a newer fixed-version manifest is published here. Automatic manifest updates are not configured.

## Current release and validation

The initial manifest installs **1.5.1**, Windows x64. Local-manifest installation, Start menu launch, uninstall and same-version reinstall were checked on an existing Windows development machine on 2026-10-20. This is not clean-machine, cross-version upgrade, existing-account-data preservation or end-to-end tunnel validation.

On the same date, adding this public GitHub bucket, searching for the package, installing `portlark/portlark-desktop`, verifying the recorded bucket source, and uninstalling also passed in a separate Scoop root. That run reused the downloaded ZIP cache and checked its SHA-256 again. The test application and Start menu shortcut were removed afterwards.

## Maintenance and reports

For a new release, verify the official versioned download URL, recompute its SHA-256 checksum, inspect the ZIP layout, and validate installation and removal before changing the manifest. Do not replace a fixed-version URL with a moving latest URL.

Report bucket installation problems in this repository's Issues with the Windows version, Scoop version and error text. Remove tokens, passwords, private URLs and account details from logs. For application or account support, use the support information on the PortLark website.

PortLark is proprietary software; its use is governed by the linked product terms. A public installation manifest does not grant rights to the application source or binaries.

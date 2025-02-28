# Windows SDK Install action

A Github Action that installs the Windows SDK in a Windows runner.

This action is based on a script available in the Windows Community Toolkit [here](https://github.com/CommunityToolkit/WindowsCommunityToolkit/blob/main/build/Install-WindowsSdkISO.ps1).

## Requirements

- A Windows runner

## What's new

Refer to the [changelog](CHANGELOG.md).

## Inputs

| Input | Required | Example | Default Value | Description |
|-|-|-|-|-|
| `version-sdk`          | Yes | 22621  | | Version of the Windows SDK to install |
| `features`          | Yes | 'OptionId.UWPCPP,OptionId.DesktopCPParm64'  | | Features of the Windows SDK to install (corresponding to the `WinSDKSetup.exe /features` switch) separated by a comma |

The available features of the Windows 10/11 SDK are:
- OptionId.WindowsPerformanceToolkit
- OptionId.WindowsDesktopDebuggers
- OptionId.AvrfExternal
- OptionId.NetFxSoftwareDevelopmentKit
- OptionId.WindowsSoftwareLogoToolkit
- OptionId.IpOverUsb
- OptionId.MSIInstallTools
- OptionId.SigningTools
- OptionId.UWPManaged
- OptionId.UWPCPP
- OptionId.UWPLocalized
- OptionId.DesktopCPPx86
- OptionId.DesktopCPPx64
- OptionId.DesktopCPParm **(removed in SDK 26100 and beyond)**
- OptionId.DesktopCPParm64

## Usage

<!-- start usage -->
```yaml
- uses: prof79/windows-sdk-install@latest
  with:
    version-sdk: 26100
    features: 'OptionId.UWPCPP,OptionId.DesktopCPParm64'
```
<!-- end usage -->

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE).

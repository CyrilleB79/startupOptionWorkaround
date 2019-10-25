# Startup option workaround

* Authors: Cyrille Bougot
* NVDA compatibility: 2017.3 to 2019.3
* Download [development version][2]

This add-on provided a work-around to solve a Windows 10 1903 issue that makes NVDA start after logon even when this option is disabled in General settings panel. On Octobre 24th 2019, Microsoft fixed the issue in KB4522355 (available via Windows Update). Thus it is recommanded to install this update.

This add-on remains available as an archive but it has become useless and should be uninstalled.

## Description of the issue

On Windows 10 1903, if NVDA is running on logon screen, NVDA will also start after login, regardless of whether the option is enabled or not for the user. This issue is described here: [#9528][3]

## Description of the workaround

When NVDA is started after logon, this add-on will check the current user's startup parameter to know if it should have started or not. If NVDA has been started whereas it should not, this add-on will cause NVDA to exit. The exit command is called just after NVDA has finished loading.

## Usage

* Just install this add-on. No specific configuration or command is required.
* As soon as NVDA or Microsoft provide a fix to the issue, this add-on becomes useless and should be uninstalled.

## Limitations

* This add-on will not prevent NVDA to load completely. Thus other installed add-ons may do some actions they would not have done if NVDA had not stated at all (licence check, sending of usage statistics, etc.)
* This add-on is not suitable for widely shared computers (university, shared workstation, etc). Indeed, a user who does not know NVDA at all will hear NVDA's startup and exit sound and see briefly NVDA's icon in the system tray. This add-on is more suitable to a computer shared with few persons (family) among which some use NVDA and other do not.
* This add-on is only a workaround. A fix in NVDA's core itself would be more adapted, as well as a Windows 10 fix from Microsoft itself.

## Change log

### Version 1.0

* Initial release.

[2]: https://github.com/CyrilleB79/startupOptionWorkaround/releases/download/V1.0-dev-20190902/startupOptionWorkaround-1.0-dev-20190902.nvda-addon

[3]: https://github.com/nvaccess/nvda/issues/9528

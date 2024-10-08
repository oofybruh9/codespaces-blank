# Content Downloader

Downlads content to make your existing OS with [EmulationStation](https://emulationstation.org), __NOT__ [ES-DE](https://es-de.org)

## Installation

Grab the latest release for your system and execute the Installer  

This is `install.sh` for Linux and `installer.exe` for Windows.

These installers will install to your `.emulationstation/cont/` folder.

Due to the installer not knowing what folder is your current theme and for safety when modifying `es_systems.cfg`, you will have to install the theme icons *__and__*  modify `es_systems.cfg` by yourself.

## Installing the icons

Get the `icons.zip`, and extract it to your current theme pack.

The file structure should look like this:

``` text

theme/
├─ theme name.xml
├─ cont/
│  ├─ theme.xml
│  ├─ icon.svg
│  ├─ bg.svg
│  ├─ the above file is only used if you set the ./theme.xml to use it
├─ etc./


```

## Modifying `es_systems.cfg`

The `es_system.xml` will have to look something like this:

```xml
<systemList>
    <!-- systems up here -->
    <system>
        <name>cont</name>
        <fullname>Content Downloader</fullname>
        <path>~/.emulationstation/cont</path>
        <extension>.sh .SH .bat .BAT</extension>
        <command>%ROM_RAW%</command>
        <platform>ignore</platform>
        <theme>cont</theme>
    </system>
    <!-- systems down here -->
</systemList>
```

## License

This is licensed under the GNU GPLv3, with parts of the code licensed under MIT.

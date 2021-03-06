# ![Icon](src/icons/icon-64x64.png) jRAT Remover
Removes any instance of jRAT on your machine running Windows, Mac OS X, Linux, *BSD, Solaris (any system running an XDG compliant desktop environment)

## How to run
Download Remover.jar and double click it or execute it using java -jar Remover.jar

## How it works

### Windows

Checks ```HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run``` for values containing java and -jar, and extracts the filename from this registry key and displaying it as possible detection. Deletes detected keys when removing.

### OS X

Checks ```~/Library/LaunchAgents/``` for plist files launching JAR files and displaying it as possible detection.
Removes this JAR and plist file when removing.

### Linux, Solaris and *BSD

Checks ```~/.config/autostart/``` for desktop entries that is made for running a JAR and displays it as possible detection.

## Dependencies

- [oslib](https://github.com/redpois0n/oslib)
- [iconlib](https://github.com/redpois0n/iconlib)
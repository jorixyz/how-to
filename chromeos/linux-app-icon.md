# How-to: Create an icon in chromeos for an app in the Linux container

## Example with intellij IDEA

Create the following file with nano as root user

```bash
sudo nano /usr/share/applications/idea.desktop
```

Or if you prefer it to be user scoped

```bash
nano /home/jorixyz/.local/shared/applications/idea.desktop
```

Paste the following content and adjust values

```ini
[Desktop Entry]
Name=IDEA    
GenericName=Java IDE        
Exec=/home/jorixyz/bin/idea
Icon=/home/jorixyz/opt/idea-IU-253.30387.90/bin/idea.png
Terminal=false
Type=Application
StartupNotify=false
Categories=Utility;
MimeType=application/java-ide;
```

Refresh the icons 

```bash
xdg-desktop-menu forceupdate
```

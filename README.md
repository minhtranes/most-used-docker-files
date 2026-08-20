# Configure podman

## Configure podman on Windows 11
** Switch to rootful mode**
To switch to root mode
```
podman machine stop
podman machine set --rootful
podman machine start
```


**Switch WSL2 to Mirrored Networking Mode (Recommended for Win 11)**
If you are on Windows 11 (version 22H2+), switching WSL from default NAT mode to `mirrored` mode shares the host's network stack directly, fixing all loopback and port-forwarding issues.

1. Open Notepad in Windows:
```cmd
notepad %USERPROFILE%\.wslconfig

```


2. Add the following lines and save:
```ini
[wsl2]
networkingMode=mirrored

```


3. Shut down WSL in PowerShell:
```powershell
wsl --shutdown

```


4. Relaunch WSL. Windows and WSL will now share the exact same network interfaces and `localhost` mapping.

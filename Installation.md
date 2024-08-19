### Installer
- Visit the [releases page](https://github.com/amnweb/yasb/releases) on GitHub.
- Look for the latest release version, which will typically be listed at the top.
- Under the "Assets" section of the release, you’ll find various files. Click on the installer file to download it.


***

### Using Python
- Install Python 3.12
- Install required Python Modules:
  - pip install -r [requirements.txt](requirements.txt)
  - Create the directory `C:/Users/{username}/.config/yasb/` and copy [styles.css](src/styles.css) and [config.yaml](src/config.yaml) into folder.
  - Configure [styles.css](src/styles.css) and [config.yaml](src/config.yaml) to your liking.
- Start the application:
  - run `python src/main.py` in your terminal (or click [yasb.vbs](src/yasb.vbs))


***

### Winget
Make sure you have installed the latest version of [winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/) and verified that installed binaries are available in your $PATH before proceeding.
Install the YASB using winget install
```
winget install AmN.yasb
```
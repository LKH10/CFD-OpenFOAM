# CFD-OpenFOAM
Tutorial doing CFD w/ OpenFOAM

## 1. Installation
Run the following code in your terminal
```
sudo sh -c "wget -O - https://dl.openfoam.org/gpg.key > /etc/apt/trusted.gpg.d/openfoam.asc"
sudo add-apt-repository http://dl.openfoam.org/ubuntu
```

If you see `add-apt-repository: command not found` error, run the following line of code and run the second line from above again. Skip this otherwise (if successful).
```
sudo apt-get install software-properties-common
```

Update your package manager with
```
sudo apt-get update
```

Finally, install OpenFOAM (OpenFOAM11 is used here). The whole installation process may take a while to complete.
```
sudo apt-get -y install openfoam11
```

To add OpenFOAM commands to your shell, open the `~/.bashrc` file with your preferred editor (nano, vi/vim, gedit, etc.) and add the following line at the bottom(, where `source` is equivalent to `.`).
```
source /opt/openfoam11/etc/bashrc
```
Restart the shell (or create a new session). Type the following to test if your configuration is done successfully.
```
foamRun -help
```
Create a directory for your projects using
```
mkdir -p $FOAM_RUN
```


# Spyder-IDE-Base (Python 3.8 64 bit Windows)
 python venv for spyder-ide and select packages for data science

I created this python environment as an alternative to Anaconda's Spyder installation, and also combined with with some of my favorite packages for geospatial and data engineering. Besides this being an easy way to get spyder working without anaconda, this is also an easy way to get Geopandas, Rasterio, and GDAL working in Windows, which can be a tough thing to do for python developers. Much love goes to [Christoph Gohlke's downloadable library of whl binaries for windows](https://www.lfd.uci.edu/~gohlke/pythonlibs/) for making many of these packages possible. This isn't meant to be the end-all best data science environment, but you're free to pip install anything you need after activating it! 

## Instructions

1. Download
2. Create a virtual environment using venv, activate it, and install from the requirements.txt like so in a command prompt:
 ```
 1 python -m venv [nameOfEnvironment]
 2 [nameOfEnvironment]\scripts\activate.bat
 3 cd [pathToWhereYouDownloadedthisRepo]
 4 pip install -r requirements.txt
 ```
 
 
## If you see this error, you need to install visual c++ build tools. 🤢
![](https://github.com/People-Places-Solutions/Spyder-IDE-Base/blob/main/Capture.PNG)

No worries, just install choco (admin cmd prompt) like so 🍫:

```
    @"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command " [System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```
👇 Then in the same command prompt run 👇:
```
    choco install -y vcbuildtools -ia "/Full" -y
```

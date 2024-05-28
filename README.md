![banner](banner.png)

# Unzip JP GUI

Unzip Japanese Shift-JIS zip archives on non-Japanese systems. This script unzips the file while converting the file names from Shift-JIS to UTF-8.

Japanese versions of Windows use Shift-JIS encoding to store file names. When a zip file is created from files containing Japanese characters and later opened on a non-Japanese system, the file names are [scrambled](https://en.wikipedia.org/wiki/Mojibake). This program aims to fix that problem.


## Usage/Examples

Run the program as described in [Run Locally](#run-locally).

  
## Run Locally

### Express

Download the latest exe file from the [release tab](https://github.com/saberzero1/unzip-jp-gui/releases) and execute it.

### Manual

Ensure you have TKinter installed if you want to run the file manually.

#### On windows:

```
python pip install tk
```

#### On Linux:

```
sudo apt-get install python3-tk 
```

execute the following command in Command Prompt from the folder
```
python archive_gui.py
```

## Unzip JP Command Line

A command-line version of the tool exists as 'unzip\_jp':

```
usage: unzip_jp [-h] [-d EXTRACTION_LOCATION] [-P PASSWORD] archive

Unzips archives containing Shift-JIS-encoded characters

positional arguments:
  archive               The archive to extract.

options:
  -h, --help            show this help message and exit
  -d EXTRACTION_LOCATION, --extraction-location EXTRACTION_LOCATION
                        Location to place the extracted files. If not given,
                        the current directory will be used.
  -P PASSWORD, --password PASSWORD
                        The password (if any) for the zip archive.
```

Can be installed by marking executable and placing in ~/.local/bin (or other $PATH location) on Linux.
No other setup is necessary, uses python standard library only.

## Acknowledgements

 - [Norbert Pozar](https://github.com/rekka/unzip-jp)

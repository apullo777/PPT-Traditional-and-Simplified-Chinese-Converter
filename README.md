# PPT-Traditional-and-Simplified-Chinese-Converter
This program is a Python script that can convert traditional Chinese text to simplified Chinese text or vice versa in a PowerPoint (PPT) file. It uses the OpenCC library for the conversion and the pptx library to read and write PPT files.

## Requirements
To use this program, you will need:

Python 3.8 or 3.9 installed on your computer (Note: this script is not compatible with Python 3.10)
The opencc-python-reimplemented and pptx Python packages installed

## Installation
1. Install Python 3.8 or 3.9 on your computer if you haven't already.

2. Install the necessary Python packages using the following command in your terminal or command prompt:

`pip install opencc-python-reimplemented pptx`

3. Download the OpenCC configuration files for traditional to simplified and simplified to traditional conversion. You can find them on the OpenCC Github page under the "data" folder.

4. Clone or download this repository to your local machine.

## Usage
1. Open the ppt_converter.py file in a text editor of your choice.

2. Set the path to the configuration file that corresponds to the conversion you want to perform in the following line of code:

```
traditional2simplified = opencc.OpenCC('/path/to/t2s/config/file')
simplified2traditional = opencc.OpenCC('/path/to/s2t/config/file')
````

3. Set the value of the t2s variable to True if you want to convert traditional Chinese text to simplified Chinese text, or False if you want to convert simplified Chinese text to traditional Chinese text:

```
t2s = True  # for traditional to simplified conversion
t2s = False # for simplified to traditional conversion
```

4. Set the path to the PPT file you want to convert in the following line of code:
```
ppt = Presentation('/path/to/pptx/file')
```

5. Open your terminal or command prompt and navigate to the directory where the ppt_converter.py file is located.

6. Run the Python file using the following command:

`python ppt_converter.py`

If you have both Python 3.8 and 3.9 installed, you can specify which version of Python to use by running one of the following commands:

`python3.8 ppt_converter.py`
`python3.9 ppt_converter.py`

7. The converted PPT file will be saved in the same directory as the original PPT file with the name "output.pptx".

## Troubleshooting
### OpenCC Configuration Error
If you encounter an error message that says "Can't find T2S/S2T configuration", it means that the OpenCC configuration file cannot be found. This may occur if you have not installed OpenCC or if the configuration file is not in the correct location.

To troubleshoot this issue, you can try the following steps:

1. Check that OpenCC is installed on your system. You can do this by running the command `pip show opencc` in your terminal. If it is not installed, you can install it using `pip install opencc`.

2. Check that the configuration file is in the correct location. The default location for the T2S configuration file is **/usr/local/share/opencc/t2s.json** on Linux/Mac or **C:\Program Files (x86)\OpenCC\share\opencc\t2s.json** on Windows. The default location for the S2T configuration file is **/usr/local/share/opencc/s2t.json** on Linux/Mac or **C:\Program Files (x86)\OpenCC\share\opencc\s2t.json** on Windows. If the file is not in this location, you may need to download it from the OpenCC GitHub repository and move it to the correct location.

3. If the configuration file is in the correct location but the error persists, you can try specifying the location of the file explicitly in the script. To do this, replace the line ```converter = opencc.OpenCC('t2s') or converter = opencc.OpenCC('s2t')``` with ```converter = opencc.OpenCC('/path/to/t2s.json') or converter = opencc.OpenCC('/path/to/s2t.json')```, where **/path/to/t2s.json** or **/path/to/s2t.json** is the absolute path to the configuration file on your system.

If you continue to experience issues, please consult the OpenCC documentation or seek help from the OpenCC community.

## Notes
- This program has been tested on macOS and should also work on Linux and Windows.
- If you encounter any issues, make sure you have followed the above steps correctly and refer to the documentation of the Python packages used for more information.
- The converted PPT file may not have the same formatting as the original file, so you may need to adjust the layout and design after conversion.

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

## Notes
- This program has been tested on macOS and should also work on Linux and Windows.
- If you encounter any issues, make sure you have followed the above steps correctly and refer to the documentation of the Python packages used for more information.
- The converted PPT file may not have the same formatting as the original file, so you may need to adjust the layout and design after conversion.

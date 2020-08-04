# FacialMotionCapture
Real-time facial motion capture in Blender 2.8 using OpenCV and a webcam.
This uses python scripting directly in Blender.

# See details here
https://youtu.be/O7nNO3FLkLU

# Installation Commands
```python
# Import sys and use sys.path to get Blender's default python path
import sys
sys.path
# Find the path from the output, something like that
/Applications/Blender.app/Contents/Resources/2.82/python/bin/python3.7m
```
```bash
# Go to the default python directory of Blender, something like that
cd /Applications/Blender.app/Contents/Resources/2.82/python/
# Use Blender's default python to install, something like that
./python3.7m -m ensurepip
./python3.7m -m pip install --upgrade pip --user
./python3.7m -m pip install opencv-python opencv-contrib-python imutils numpy dlib --user
```
# Blender Cloud
https://cloud.blender.org/p/characters

# Facial landmarks database
http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2

# Issue
- dlib installation failed
```bash
brew install dlib
brew install cmake
# Use Blender's default python to install, something like that
./python3.7m -m pip install boost
./python3.7m -m pip install cmake
```
- Python.h not found.
```bash
# Install same version of your Blender's default python version, something like that
brew install python@3.7
brew link python@3.7
# Find Python.h
sudo find / -iname "Python.h"
# "your_python_directory" is the directory of your Python.h location
export C_INCLUDE_PATH=${your_python_directory}
export CPLUS_INCLUDE_PATH=${your_python_directory}
```
- When "Capture" button is clicked, Blender turns off
```bash
# Open Blender using the command line, something like that
/Applications/Blender.app/Contents/MacOS/Blender
```
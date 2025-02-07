# AS1170 Python Library

## Description
This library allows control of the **AS1170** driver via **I2C** on **Raspberry Pi**, enabling LED management with simple commands like `led1.on()` and `led1.off()`.

## Installation
Since Raspberry Pi OS has stricter package management, it is recommended to install the library in a virtual environment to avoid conflicts.

### 1?? Install Python Virtual Environment
If `venv` is not installed, run:
```sh
sudo apt install python3-venv
```

### 2?? Create a Virtual Environment
Inside your project folder:
```sh
python3 -m venv venv
```

### 3?? Activate the Virtual Environment
```sh
source venv/bin/activate
```

### 4?? Install the Library
```sh
pip install as1170
```

### 5?? Using the Library
```python
from as1170.driver import led

led.on()
time.sleep(1)
led.off()
```

### 6?? Deactivate the Virtual Environment
```sh
deactivate
```

## Uninstallation
To remove the library from your virtual environment:
```sh
pip uninstall as1170
```
If you want to completely remove the virtual environment:
```sh
rm -rf venv
```

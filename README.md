# AS1170 Python Library

## Description
This library allows control of the **AS1170** driver via **I2C** and a **GPIO Pin** for **Strobe control** on **Raspberry Pi**, enabling LED management with simple commands like `led.on()` and `led.off()`. It also supports adjustable intensity and a strobe mode.
This library takes for granted that the **AS1170** id is
## Installation
Since Raspberry Pi OS has stricter package management, it is recommended to install the library in a virtual environment to avoid conflicts.

### 1 Install Python Virtual Environment
If `venv` is not installed, run:
```sh
sudo apt install python3-venv
```

### 2 Create a Virtual Environment
Inside your project folder:
```sh
python3 -m venv venv
```

### 3 Activate the Virtual Environment
```sh
source venv/bin/activate
```

### 4 Install the Library
```sh
pip install as1170
```

### 5 Using the Library
```python
from as1170 import led

# Set LED intensity (in mA, range 0-450mA. Default led1=450 , led2=450)
led.set_intensity(led1=300, led2=200)

# Turn LEDs on
led.on()

# Wait for 1 second
time.sleep(1)

# Turn LEDs off
led.off()
```

### 6 Using the Strobe Mode
```python
# Start strobe mode at 5 Hz (flashes until stopped manually)
led.strobe(frequency=5)

# Wait for 10 seconds while strobe is running
time.sleep(10)

# Stop the strobe and turn LEDs off
led.off()
```

### 7 Deactivate the Virtual Environment
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


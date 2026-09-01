# Real HDD Simulator

A realistic hard disk drive (HDD) storage simulator built with Python and Kivy.

The simulator visually represents how a traditional mechanical HDD works, including a rotating platter, read/write head movement, tracks, sectors, used storage areas, free storage areas, storage capacity, and simulated HDD activity.

It also maintains real files and folders in the simulator's storage directory while using a virtual 1 GiB storage model to determine whether new data can be stored.

---

## Features

- Realistic HDD-style graphical interface
- Rotating disk platter
- Mechanical read/write head movement
- Tracks and sectors visualization
- Used and free storage visualization
- Red storage indicators
- Storage usage increases as data is stored
- Virtual HDD capacity of exactly 1 GiB
- Supports files and folders
- Synchronizes the simulator with external storage files
- Detects newly added files
- Detects deleted files
- Simulates storage allocation
- Stops accepting new data when the virtual HDD becomes full
- HDD activity simulation
- Real file and folder storage
- Kivy-based graphical interface
- Designed to work on Android with Pydroid 3

---

# Installation

## Pydroid 3

Install Python 3 and Kivy support in Pydroid 3.

Then open the Pydroid 3 terminal and install the simulator:

```bash
pip install real-hdd-simulator
```
After installation, the simulator package will be available in Python.
Running the Simulator
The recommended way to run the graphical interface in Pydroid 3 is to create a Python file.
For example:
run_hdd.py
Put this code inside the file:
from kivy.app import App
from hdd_simulator.main import HDDSimulatorApp

app = HDDSimulatorApp()
app.run()
Save the file.
Then open it with Pydroid 3 and press the Run button.
Enjoy the HDD storage simulation!
Quick Start
After installing:
pip install real-hdd-simulator
Create:
run_hdd.py
with:
from kivy.app import App
from hdd_simulator.main import HDDSimulatorApp

app = HDDSimulatorApp()
app.run()
Run the file using Pydroid 3.
Storage
The simulator uses a virtual HDD with a capacity of exactly:
1 GiB
The virtual capacity is independent from the amount of physical free storage available on the Android device.
The simulator uses the storage directory to maintain the files and folders associated with the virtual HDD.
The virtual HDD determines whether the simulated disk has enough available space.
Files and Folders
The simulator supports normal files and folders.
The storage directory is created automatically.
Depending on the Android environment, it may be created in the shared Android storage area as:
/storage/emulated/0/HDD_Simulator_Storage/
The simulator can monitor this directory and synchronize its virtual storage state with files found there.
Virtual HDD Image
The simulator creates:
virtual_hdd.bin
This file belongs to the simulator's virtual disk system.
It is used for the virtual HDD representation and disk structure.
The simulator also maintains metadata describing the virtual disk state.
How the HDD Simulation Works
The virtual HDD is modeled using:
Tracks
Sectors
Logical block addresses (LBA)
Sector allocation
Rotational position
Rotational latency
Seek movement
Read/write activity
The platter rotates continuously while the simulated read/write head moves across tracks.
The graphical interface displays the current HDD activity.
Storage Visualization
The disk visualization represents storage areas using individual sectors.
Empty storage areas are displayed as unused areas.
Used sectors are represented using red indicators.
As more virtual storage is consumed, the red storage indicators become more visible.
When the virtual disk approaches full capacity, the visualization reflects the increased storage usage.
Full Disk Behavior
When the virtual HDD reaches its 1 GiB capacity:
1 GiB / 1 GiB
the simulator stops accepting additional virtual data.
Existing files remain available.
To make space available again, delete files from the simulator's storage area.
After enough storage has been freed, the virtual HDD can accept new data again.
Important Note
The simulator is a software simulation.
It does not control or physically operate the Android device's real HDD hardware.
The platter rotation, head movement, sectors, seek time, rotational latency, and storage allocation are simulated in software for educational and visualization purposes.
Requirements
Python 3
Kivy 2.3.0 or newer
Pydroid 3 on Android
Android storage permission when required
Example
Install:
pip install real-hdd-simulator
Create:
run_hdd.py
Content:
from kivy.app import App
from hdd_simulator.main import HDDSimulatorApp

app = HDDSimulatorApp()
app.run()
Run it in Pydroid 3.
Project Structure
A typical installation contains:
hdd_simulator/
    __init__.py
    main.py
The package provides:
HDDSimulatorApp
and the application entry point:
main()
Educational Purpose
This project is intended to demonstrate concepts related to mechanical hard disk drives, including:
Magnetic storage concepts
Disk geometry
Tracks
Sectors
Logical block addressing
Disk allocation
Rotational latency
Seek time
Storage utilization
File system synchronization
Virtual storage devices
It is designed as an interactive visualization rather than a replacement for a physical storage device.
License
See the project's license file for licensing information.
Enjoy
Install the package, create the small launcher file in Pydroid 3, run it, and enjoy the mechanical HDD simulation!
from kivy.app import App
from hdd_simulator.main import HDDSimulatorApp

app = HDDSimulatorApp()
app.run()
Enjoy the HDD storage simulation!

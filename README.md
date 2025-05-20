
## Installation
1. Clone the powerloss recovery Klipper repository from GitHub to your local machine:
```bash
git clone https://github.com/inzaneone/plr-klipper.git
cd plr-klipper
./install.sh
```

###start-gcode add in your slicer:
```bash
G31
save_last_file
SAVE_VARIABLE VARIABLE=was_interrupted VALUE=True
```

###end-gcode add in your slicer:
```bash
SAVE_VARIABLE VARIABLE=was_interrupted VALUE=False
clear_last_file
G31
```
###Before layer change G-gcode add in your slicer:
```bash
LOG_Z
```
6. To resume printing after a power cut, simply execute the 'RESUME_INTERRUPTED' macro in the MAINSAIL console or via the Macro button on the MAINSAIL dashboard.

## Known Bugs:
The preview image of the gcode file is not rebuilt.
 





## Welcome to G4Eye
G4Eye is an application based on the Geant4 Monte Carlo toolkit for simulating the interaction of various types of radiation (e.g. external gamma-rays or Tritium) as they pertain to the lens of the eye. 

## Build Notes
To build this application, you should have a working version of CMake
and Geant 4.10.3.p01 or higher.

Geant4: https://geant4.web.cern.ch/geant4/ CMake: https://cmake.org/

I recommend setting up your directory structure as follows:

- $G4WORKDIR/G4Eye : This is the source directory and is a clone of the code from this GitHub 
- $G4WORKDIR/G4Eye-build : Contains directories and files for each build. This directory also contains the executable files and example macros.

The simulation works both in sequential and in multi-threaded (MT) modes of Geant4. However, a significant speedup can be achieved by running the simulation in MT mode.

## Steps to compile:
### Step 1 - Source the Geant4 environment setup script
### NOTE: You'll need to change the version of Geant4 in the path

    source /opt/Geant4/geant4.10.03.p01-install/bin/geant4.sh

### Step 2 - Create the build directory and navigate to it
    
    mkdir G4Eye-build && cd $_

### Step 3 - Setup CMake, make the build, and run the build

    sudo cmake -DGeant4_DIR=/opt/Geant4/geant4.10.03.p01-install/lib/Geant4-10.3.1/ ~/G4WORK/G4Eye; sudo make -j8; ./G4Eye


To recompile, I typically just re-run the command in Step 3

## Scoring Physical Quantities
TODO: Update this section once simulation is complete.


# Amnesia on ARM
This is just a little experiment I'm doing to port Amnesia: The Dark Descent on ARM/aarch64-based devices, specifically the Raspberry Pi 4

The other fork I saw which was specifically made for linux/bsd started having frantic compiler errors and issues on my end, so i thought forking the TiManGames/AmnesiaTheDarkDescent repo would be good enough since ive had very few errors besides not being able to compile due to the broken symlinks i had earlier. Let's hope I can fix them

Currently it will only support building binaries for Linux since it's easier to make ARM builds this way

## Prerequisites
- A copy of Amnesia: the Dark Descent (For playing the game, many files necessary for launching don't come with the source code)
- CMake, Make (for compiling)

### Engine Overview
Todo: Add some descriptions about what kind of files we have in the engine solution.

### Game Overview
Todo: Add some descriptions about what kind of files we have in the game solution.

## Building & Playing (Linux)
There are a few extra steps required to be able to successfully build everything on Linux compared to Windows.

### Building the Engine, Game & Editors
1. Ensure you have `make` and `cmake` installed.
2. Go to lxterminal and type `git clone https://github.com/RoozerXC/AmnesiaOnARM`
3. Navigate to `AmnesiaOnARM/HPL2` and `unzip dependencies.zip`
4. Run the script file at `./HPL2/dependencies/lib/linux/lib64/fix_symlinks.sh` to fix broken symlinks from the .zip file
5. In the `AmnesiaOnARM/amnesia/src` directory run `cmake .`
6. Type `make` (or use `make -jX` where X is the number of jobs you want to run to speed things up, based on your CPU threads)
7. The build should compile and the resulting binaries will be found in `./amnesia/src`

### Playing the Game
To run the compiled binary, copy it to your Amnesia installation folder. For example copy the `Amnesia.bin.x86_64` to your game folder. Run it, and the game should start directly.

## License Information
All code is under the GPL Version 3 license. Read the LICENSE file for terms of use of the license.

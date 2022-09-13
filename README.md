# rsekhar2-gomes3-cthu2-cortiz42
Repo for rsekhar2-gomes3-cthu2-cortiz42

### Initial Setup
To use the provided VSCode build tasks, clone the repo wiht the following command:
```
$ git clone https://github-dev.cs.illinois.edu/cs225-fa21/rsekhar2-gomes3-cthu2-cortiz42.git ~/sfpa
```
This project uses CMake for its Makefile configuration, requiring an initial run of the `cmake` command upon cloning.
```
$ cd ~/sfpa/bus-mapper
$ mkdir build
$ cd build
$ cmake ..
```

### Building & Running

A number of VSCode tasks are available using the Build command (shortcut : `Ctrl`/`CMD`+`Shift`+`B`), such as:
 - Build Pathfind
 - Build Visualize
 - Build Tests
 - Run Tests
 - Reload CMake
 - Format

Targets can also be built normally from the command line, and are all located in the `build` directory.
```
$ cd ~/sfpa/bus-mapper/build
$ make pathfind
$ ./pathfind FROM_STATION_ID TO_STATION_ID
$ make visualize
$ ./visualize output.png [-f]
$ make test
$ ./test
```
Available targets for build are: `pathfind`, `visualize` and `test`

Note: `[-f]` is the optional flag for force-firected drawing


### Adding/Deleting/Renaming a File

Due to our use of file-searching in CMake, any of the above changes which affect file names will need you to trigger a CMake reload in one of the following ways:
 - Using the `Reload CMake` VSCode task accessible via the Build command (shortcut : `Ctrl`/`CMD`+`Shift`+`B`).
 - Running the command `touch <directory>/CMakeLists.txt` for any any CMakeLists.txt file in the project.
 - Opening and saving (with no changes) any CMakeLists.txt file in the project.

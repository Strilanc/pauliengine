# SymEngine Installation and Build Guide (Windows)

## Prerequisites

- **Visual Studio** (with C++ build tools)  
  During installation, make sure to select:  
  - **Desktop development with C++** workload

- **Git** installed and accessible from the command line

- **CMake** installed and added to your PATH

---

Step 1 install conan via pip install conan

isntall symengine:
conan install --requires="symengine/[*]"


in project directory (if no build directory)
conan install . --output-folder=build --build=missing

cd build

cmake .. -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake -G "Visual Studio 17 2022" -A x64


cmake --build . --config Release
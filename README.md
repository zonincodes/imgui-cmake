# IMGUI_CMAKE

This is a simple cmake starter project for imGUI and GLFW on Ubuntu.

## Installation 

```bash 
git clone https://github.com/zonincode/imgui-cmake --recurse-submodules

#git submodule foreach git pull origin head

mkdir build && cd buld
cmake --buld .
./imgui-setup
```

# Ubuntu Support

## Building
* You may need these dependencies:
```bash
sudo apt-get install libglfw3 libglfw3-dev xorg-dev
```
# Vulkan Tutorials from Khronos

This is the tutorial created while reading the Vulkan Tutorial page from Khronos.

The example starts from main_v1.cpp to the last. main.cpp will be the same as the last version. For example, if the last is main_4.cpp, then main.cpp will be the same as main4.cpp

### For Windows

1. First open the VulkanTest.sln at the build directory
2. Add the library path in the linker
3. Add the library to the linker
   1. vulkan-1.lib
   2. glfw3.lib
4. Add Include folder to the project
5. Compile to test
6. On Command Line, type this after saving the sln file: cmake .. && cmake --build . --target VulkanTest

Update: 
* You can now compile using cmake
```
   cd build
   cmake .. && cmake --build . --target VulkanTest
```

### For Linux

1. Install vulkan-sdk
   wget -qO- https://packages.lunarg.com/lunarg-signing-key-pub.asc | sudo tee /etc/apt/trusted.gpg.d/lunarg.asc
   sudo wget -qO /etc/apt/sources.list.d/lunarg-vulkan-1.3.283-jammy.list https://packages.lunarg.com/vulkan/1.3.283/lunarg-vulkan-1.3.283-jammy.list
   sudo apt update
   sudo apt install vulkan-sdk
   sudo apt install libglfw3
   sudo apt install libglfw3-dev
   sudo apt install libglm-dev
2. Install mesa tools
   sudo apt install mesa-utils
3. Test if GPU can be seen
   glxinfo -B
4. set DISPLAY
   export DISPLAY=:0.0
5. Run vkcube. If this ok, then you are ok.

This repo also included a Makefile for you to use with make command

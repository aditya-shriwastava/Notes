# Cliene libraries

## Workspace

* A ROS workspace is a directory with a particular structure.
* Commonly there is a src subdirectory. Inside that subdirectory is where the source code of ROS packages will be located.
* By default it will create the following directories as peers of the src directory:
  * **build:** where intermediate files are stored.
  * **install:** where each package will be installed to. 
  * **log:**  directory contains various logging information about each colcon invocation.
* Compared to catkin there is no devel directory.

## Creating a package

* A package can be considered a container for your ROS 2 code.
* Package creation in ROS 2 uses:
  + **ament** as its build system and
  + **colcon** as its build tool.
* You can create a package using either CMake or Python:
  * CMake:
    * **package.xml:** file containing meta information about the package
    * **CMakeLists.txt**: file that describes how to build the code within the package
  * Python:
    * **package.xml:** file containing meta information about the package
    * **setup.py:** containing instructions for how to install the package
    * **setup.cfg:** is required when a package has executables, so ros2 run can find them
    * **/<package_name>:** a directory with the same name as your package, used by ROS 2 tools to find your package, contains `__init__.py`

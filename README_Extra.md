## Issues

When installing on Linux, you will need to install the a couple of Python packages in the Python runtime of Blender in order for the plugin to be loaded properly, to do so use the following commandsto istall `pip` to the Blender Python runtime:

```sh
cd [Blender main folder]/x.y/python # x is the major version and y is the minor version of Blender, e.g. 3.1
wget https://bootstrap.pypa.io/get-pip.py
./bin/python3.x ./get-pip.py --prefix [absolute path of current folder] # x is the minor version of Python 3
```

Once this is done, the Blender pip can be used to install the necessary packages:

```sh
./bin/python3.x bin/pip3 install rospkg # x is the minor version of Python 3
./bin/python3.x bin/pip3 install urdf_parser_py # x is the minor version of Python 3
```
This allows the plugin to be loaded in Blender.

## **NOTICE**

Always be sure that ROS is being sourced in the terminal where you run Blender.
On Windows, even after the plugin is loaded, it will still give a sourcing error when importing files as ROS1 cannot be natively installed and sourced.
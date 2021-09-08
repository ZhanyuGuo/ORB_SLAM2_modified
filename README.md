# Update for unpacked ROB_SLAM with pcl view repo

## Build:

### Build the whole project ( inclouding binary loading tools ):

Before all the cmd, **DONOT** forget to download the Vocabulary form the [origin repo](https://github.com/raulmur/ORB_SLAM2) and place it into dir ./Vocabulary, and also config 3rdparty reposities such as OpenCV, Eigen, etc.

```bash
     cd YourDirectory/ORB_SLAM2_modified
     chmod +x build.sh
     ./build.sh
```

### Only build the ORB_SLAM2 mode with pcl

```bash
    cd YourDirectory/ORB_SLAM2_modified
    mkdir build
    cd build
    cmake ..
    make -j4
```

## Run:

```bash
    ./bin/rgbd_tum Vocabulary/ORBvoc.bin path_to_settings  path_to_sequence path_to_association
```

# What are modified (by Gao Xiang):

* changing the vocabulary loading method into binary mod

* adding a pointcloud viewer( realized by adding a viewer thread )

* changing the CMakeLists.txt that all the executable files are placed in ./bin

# What are modified (by Guo Zhanyu):

* change the gray pointcloud to a colorful one.

* save pointcloud file automatically.

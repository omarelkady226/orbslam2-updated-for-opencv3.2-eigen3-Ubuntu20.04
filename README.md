# orbslam2 Updated for OpenCV3.2 & the updated Eigen3 for Ubuntu20.04
I had some problems with using orbslam2 with the updated dependencies, specifically Eigen3 and OpenCV3.2. It took some time to change some of the files to get it to build. This is a repository to keep these changes

This code all belongs to orbslam2. I just uploaded the files that need changing in order to make a successful build.

I used Pangolin v0.5, OpenCV3.2 and the newest version of Eigen3 as of June 2022. This was all tested on Ubuntu 20.04.

# Instructions

After cloning orbslam2 into any folder on your Linux device change the include, examples and src folders with the ones provided in the library. Next, change the CMakeLists.txt in the orbslam2 folder with the one provided.

Then go to /Thirdparty/g20/g20/solvers and change linear_solver_eigen.h with the one provided.
Finally change the CMakeLists.txt in Thirdparty/DBoW2 with the one provided. Note that you have to remove DBoW2_ from the name of the file provided so that it is just CMakeLists.

If any errors arise it will probably be due to the opencv3.2 path that I provided on my system. If that is the case, go to the files that show the error and find the line that starts with "FindPackage(OpenCV3.2 " < file path > ") and change the file path to the opencv build path

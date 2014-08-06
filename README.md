 
 ************************************************************************************************
 
 From Design to Software 2
 
 Miroslav Byrtus
 1328167
 
 ************************************************************************************************
 
 Description 
 
 PCL Integration in Unity 

 Unity: 
 * Load pointclouds (from file / kinect)
 * Segment
   + Plane model segmentation (floor segmentation)
     http://pointclouds.org/documentation/tutorials/planar_segmentation.php#planar-segmentation) 
   + Euclidean Cluster Extraction (object segmentation)
     http://pointclouds.org/documentation/tutorials/cluster_extraction.php#cluster-extraction)
   + Store indices of segmented clusters 
 * Display 
   + enable in scene (arrows + mouse)
 * Make clusters (segmented pointclouds) clickable 
   + after clicking on cluster - mark it and enable movement ( w a s d )
 
 ------------------------------------------------------------------------------------------------
 
 Requirements for compiling the project from source code: 

   * PCL 1.7 installed on your PC 
   ** To install PCL, follow the steps on the official website, according to your OS 
      + http://pointclouds.org/downloads/linux.html
      + http://pointclouds.org/downloads/windows.html
      + http://pointclouds.org/downloads/macosx.html

 For development:
   * Unity3D (free version is enough)
   * MS Visual Studio - version compatible with PCL installed
 
 Optional:
   * Kinect
   ** If you want to use Kinect in this project, you also will need to install
      + drivers for Kinect for your OS 
      + OpenNI (In the list of optional dependencies for PCL)
 
Requirements for running the project: 
  
   * Unity3D (free version is enough)
   * Unity Project 
   * cpp_plugin_pcl.dll coppied into the root directory of the project 
   * dependent ddls for cpp_plugin_pcl.dll (Can vary depending on PCL version installed and on your OS)
     For Windows 8 32bit with PCL 1.7. 32bit installed, it is: 
     + kernel32.dll
     + advapi32.dll
     + pcl_common_debug.dll
     + pcl_io_debug.dll
     + pcl_search_debug.dll
     + pcl_filters_debug.dll
     + pcl_segmentation_debug.dll
     + msvcp100d.dll
     + msvcr100d.dll
   * If you want to use Kinect in this project, you also will need drivers for Kinect, compatible with your OS 
   
 ------------------------------------------------------------------------------------------------
 
 How to use the plugin? 
 
 1. Create a DLL from the .cpp file 
 2. Make sure that the DLL is located in the root folder of your Unity Project (Copy it in Filesystem, not trough Unity)
 3. Copy the pointcloud file into the project directory, or connect Kinect to your PC
 3.1. If you want to use Kinect, you have to check the "Use Kinect" checkbox in the Plugin Script settings
      If it's not checked, it will load a Pointcloud from file "table_scene_lms400.pcd" (It's available in the UnityPCL directory)
 4. Now you can use the plugin (Check the example script how to use it's functionality)
 
 ------------------------------------------------------------------------------------------------
 
 

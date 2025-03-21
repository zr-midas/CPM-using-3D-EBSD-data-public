# Process 3D-EBSD data for CPM

The Dream.3D pipeline in this folder contains the sequence of filters that outputs a 3D microstructure without precipitates and with clean and homogeneous grains. 

The filters used for each stage of the data processing are described below:

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Stages of the 3D data processing</summary>
  <ol>
    <li><a href="#1-reconstruction">Reconstruction</a></li>
    <li><a href="#2-cleaning">Cleaning</a></li>
    <li><a href="#3-remove-hydrides">Remove hydrides</a></li>
    <li><a href="#4-Zr-grains-homogenisation">Zr grains homogenisation</a></li>
  </ol>
</details>

<!-- reconstruction -->
## 1. Reconstruction

The reconstruction includes:
- Some filters to rotate the data as needed. The rotations applied depend on the equipment used and the orientation of the sample. The filter "Rotate Sample Reference Frame can be used" too if necessary.
- Some filters to get the data ready for alignment
- A filter for the alignment
- A filter for the grain segmentation
- Some filters to export texture plots to see the changes produced with the rotation
- A filter to write all the data into a dream3d file with a xdmf file for visualisation

![image](https://github.com/user-attachments/assets/4e3171d6-bb34-478b-b229-d81001d0b01f)

<!-- cleaning -->
## 2. Cleaning

![image](https://github.com/user-attachments/assets/175c8c30-897a-4957-aa99-e69ca5481159)


<!-- remove-hydrides -->
## 3. Remove hydrides

![image](https://github.com/user-attachments/assets/280db4b9-638c-422a-a83c-696b8cd2db70)


<!-- Zr-grains-homogenisation -->
## 4. Zr grains homogenisation

![image](https://github.com/user-attachments/assets/ca22f76a-0ac4-4cf8-8e0d-a91afb72094d)




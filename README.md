# CPM-using-3D-EBSD-data

This repository contains the methodology for running crystal plasticity simulations (CPM) on a representative volume element (RVE) generated from 3D-EBSD data

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Folders</summary>
  <ol>
    <li><a href="#Process-3D-EBSD-for-CPM">Process 3D-EBSD for CPM</a></li>
    <li><a href="#Produce-RVE-from-3D-EBSD">Produce RVE from 3D-EBSD</a></li>
    <li><a href="#Damask-simulations">Damask simulations</a></li>
    <li><a href="#MatFlow-simulations">MatFlow simulations</a></li>
  </ol>
</details>


<!-- Process-3DEBSD-for-CPM -->
## [Process 3D-EBSD for CPM](./Process-3D-EBSD-for-CPM/)

This folder contains a Dream.3D pipeline with a sequence of filters that outputs a 3D microstructure without precipitates and with clean and homogeneous grains. 

The filters used for each stage of the data processing are described in the Readme file of this folder.

<!-- Produce_RVE_from_3DEBSD -->
## [Produce RVE from 3D-EBSD](./Produce-RVE-from-3D-EBSD/)

This folder contains a Python script for producing a representative volume element (RVE) needed to run the CP simulations.

The RVE is described by two files: material.yaml (with all the orientations in the RVE) and geom.vtr (with the geometry of the RVE)

The script in this folder produces these two files using the data imported from a dream3d file. The method for obtaining the desired microstructure from the raw 3D-EBSD data is in: [Process 3D-EBSD for CPM](./Process-3D-EBSD-for-CPM/).

<!-- Damask-simulations -->
## [Damask simulations](./Damask-simulations/)

This folder contains the script and input files needed to run the CP simulations using the RVE produced ([Produce RVE from 3D-EBSD](./Produce-RVE-from-3D-EBSD/)).

It also includes a script to extract visualisation files from the data file exported from the model.

<!-- MatFlow -->
## [MatFlow simulations](./MatFlow-simulations/)

[MatFlow]([https:/docs.matflow.io/stable/) is an open-source software that merges, via extensions, material simulation kits and libraries to connect the single crystal behaviour to the macroscopic mechanical response of the material. 

This folder contains the script used in MatFlow to run cooling CP simulations, as well as some examples of the input files needed (the RVE files produced in [Produce RVE from 3D-EBSD](./Produce-RVE-from-3D-EBSD/)).

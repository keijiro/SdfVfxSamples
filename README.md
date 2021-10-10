VectorFieldExamples
===================

This repository contains examples that show how to use vector fields with
Unity Visual Effect Graph.

![screenshot](https://i.imgur.com/SrcqEPzm.jpg)
![gif](https://i.imgur.com/lCocilb.gif)

![gif](https://i.imgur.com/iUGn7Fw.gif)
![gif](https://i.imgur.com/jPluUSJ.gif)

System requirements
-------------------

- Unity 2021.2
- HDRP 12.0

How to export a volume from Houdini
-----------------------------------

Firstly, you have to install `Unity_VFX_Tools.hda` to your project. Download
and import it from the [VFXToolbox] repository.

[VFXToolbox]:
  https://github.com/Unity-Technologies/VFXToolbox/tree/master/DCC-Tools%7E/Houdini

You can export a `.vf` file using Volume Exporter SOP. There are a few things to
take care of:

- It only supports the standard volume. If you're using a VDB volume, you have
  to convert it to a standard one.
- It only supports uniformly sized volume (x size == y size == z size). You may
  have to resize it before exporting.
- The default wrap mode of `.vf` file is "repeat." It should be changed to
  "clamp" when using a distance field volume.

For details, please see the example Houdini project contained in the
[`Houdini`](Houdini) directory.

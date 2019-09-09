# ChiLL, the node-based editor for IceSL

![ChiLL banner][banner]

## What is Chill?
Chill is a **node-based editor** for [**IceSL**, the **Modeler and Slicer**](https://icesl.loria.fr).

Created by members of the team behind IceSL, ChiLL is a tool which aims to provide a **Visual Programming** interface for IceSL.

As IceSL offers the possibility to directly create models using Lua scripting, ChiLL will provide a way to create those modeling scripts using an approach based on Visual Programming. No need to code or learn the scripting language!

>**Note**
>ChiLL is easily extendable, as all nodes are themselves IceSL scripts.

## How to install ChiLL?

>**Note**
>First and foremost, install [IceSL](https://icesl.loria.fr/download/).
>Once IceSL is installed on your machine, you have everything required to run a pre-compiled version of Chill!

### On Windows
For Windows users, ChiLL is available through an **installer** (an .exe or .msi), or by retrieving the source code and **building the project**.

### On Linux
For Linux users, ChiLL is only available through retrieving the source code and **building the projet**.

Installers and pre-compiled versions of ChiLL will be provided in future releases.

## How to build ChiLL?
To build ChiLL, you will need the following components installed on your computer:

- git
- CMake
- C++ 17 standard libraries
- Any IDE supporting C++ (on windows, Visual Studio is recomended)

Once the required components installed, you can fetch the source code by cloning or dowloading a .zip of the source files.

```Shell
git clone https://github.com/shapeforge/Chill.git
```

Initialize and fetch the submodules dependencies.

```Shell
git submodule init
git submodule update
git submodule foreach git pull origin master
```

You can now build the project for your IDE of choice using CMAKE, and then compile.

## How to Use ChiLL?
Once ChiLL is opened -- and IceSL alongside it -- you can access a menu containing the different nodes by doing a right-click.

![Nodes Menu][node_menu]

There you can select an input-node.

![Using an input-node][input_node]

You can now select an output-node and link the nodes. To do this click and drag a link from the output of the first node to the input of the second node.

![Linking nodes][linking_nodes]

At launch time, ChiLL opens IceSL to produce a real-time preview of the model generated by the nodes. You can modify the parameters of any node interactively by typing or dragging values. The modifications are immediately reflected in the live preview of the object rendered in IceSL.

![Live preview with IceSL][live_preview]

Once the graph is complete, you can save it for later, or export a .lua file tailored for IceSL.

## How to contibute to ChiLL?
### New features or reworking the project
Create your own fork of the projet, and submit a [pull request](https://github.com/shapeforge/Chill/pulls). 
>**Note**
>When contributing using a pull request, don't hesitate to be precise in the description of your contribution, and don't forget to document what you did.
>It will greatly help us to intergrate your changes! 

### Bug reports and feature requests
If you encounter a bug, or have an idea for a new feature, please fill an [issue](https://github.com/shapeforge/Chill/issues), so we can discuss about it.
>**Note**
>Please be as precise as possible when filling an issue. For bug reports, please join some scripts/files that reproduce the problem.
>Using a label on your Issue will greatly help us tracking and processing them.

# Credits
Main developpers:

- Jimmy Etienne [[@JuDePom](https://github.com/JuDePom)] 
- Pierre Bedell [[@Phazon54](https://github.com/Phazon54)] 
- Thibault Tricard [[@ThibaultTricard](https://github.com/ThibaultTricard)] 
- Cedric Zanni [[@czanni](https://github.com/czanni)] 

Logos:

- Pierre-Alexandre Hugron

Acknowledgements:

Special thanks to the [IceSL devs](https://icesl.loria.fr/about/) and in particular Salim Perchy [[@ysperchy](https://github.com/ysperchy)] for his help!

ChiLL initial development was supervised by Sylvain Lefebvre [[@sylefeb](https://github.com/sylefeb)]. 
It is inspired by an earlier prototype by Jean Hergel [[@jhergel](https://github.com/jhergel)]. 

Feel free to join us in improving ChiLL!

External libraries and tools used:

- [dear imgui](https://github.com/ocornut/imgui)
- [LibSL](https://github.com/sylefeb/LibSL)
- [lua5.1](https://www.lua.org/versions.html)
- [luabind-deboostified]
- [tinyfiledialogs](https://github.com/native-toolkit/tinyfiledialogs)

Funding:

ChiLL initial development was mainly supported by the ERC ShapeForge (StG-2012-307877) and [Inria](https://www.inria.fr/en/).

[//]: # (Ressources)
[banner]: ressources/images/chill_banner_wide_medium.png
[node_menu]: ressources/images/gifs/nodemenu.gif
[input_node]: ressources/images/gifs/inputnode.gif
[linking_nodes]: ressources/images/gifs/linknode.gif
[live_preview]: ressources/images/gifs/preview.gif

# ChiLL, the node-based editor for IceSL

![ChiLL banner][banner]

## What is Chill?
Chill is a **node-based editor** for [**IceSL**, the **Modeler and Slicer**](https://icesl.loria.fr).

Created by members of the team behind IceSL, ChiLL aims to provide a **Visual Programming** interface for IceSL.

Because IceSL offers the possibility to directly create models using Lua scripting, ChiLL provide a way to create those modeling scripts using an approach based on Visual Programming. No need to code or learn the scripting language!

>**Note**
>ChiLL is easily extendable, all nodes are IceSL scripts themselves.

## How to install ChiLL?

>**Note**
>First and foremost, install [IceSL](https://icesl.loria.fr/download/).
>Once this is done, you have everything required to run a pre-build version of Chill!

### Pre-build versions
For both [Windows][win_zip] and [Linux][linux_zip] based systems, ChiLL is available as a **.zip** containing pre-build executables and nodes to provide a quick start!

### Installers

#### On Windows
For Windows users, [.msi][win_msi] installer is available.

#### On Linux
For Linux users, a [.deb][deb_install] is available for **Debian-based** distributions.

### From Source
ChiLL can also be used direcly from the source code, by **building and compiling** the project manually. To do so, please [see the section below](#build-chill).

## How to build ChiLL? <a name ="build-chill"> 
To build ChiLL, you will need the following components installed on your computer:

- git
- CMake
- C++ 17 standard libraries
- Any IDE supporting C++ (on windows, Visual Studio is recommended)

Once the required components installed, you can fetch the source code by cloning or downloading a .zip of the source files.

```Shell
git clone https://github.com/shapeforge/Chill.git
```

Initialize and fetch the submodules dependencies.

```Shell
git submodule update --init --recursive

git submodule update --recursive --remote 	# with git 1.8.2 or above
# or
git submodule update --recursive			# with git 1.7.3 or above
```

Then you can, if you want, fetch the latest changes of each submodule.

```Shell
git pull --recurse-submodules
```

You can now build the project for your IDE of choice using CMAKE, and then compile.

## How to Use ChiLL?
Once ChiLL is opened -- and IceSL alongside it -- a menu containing the different nodes  is displayed in the left side-bar of ChiLL.

You can also access the nodes by doing a right-click on the working space.

![Nodes Menu][node_menu]

To create a graph, start by creating a new node on the workspace, using the nodes menu..

![Using an input-node][input_node]

You can now create an emit-node and link the nodes. 

To do this click and drag a link from the output of the first node to the input of the second node.

![Linking nodes][linking_nodes]

At launch time, ChiLL opens IceSL to produce a preview of the geometry generated by the nodes. You can modify the parameters of any node interactively by typing or dragging values. The modifications are immediately reflected in the preview of the object rendered in IceSL.

![Live preview with IceSL][live_preview]

You can then save the produced graph for later use, or you can export it as a .lua file tailored for IceSL.

## How to contribute to ChiLL?
### New features or reworking the project
Create your own fork of the project, and submit a [pull request](https://github.com/shapeforge/Chill/pulls). 
>**Note**
>When contributing using a pull request, don't hesitate to be precise in the description of your contribution, and don't forget to document what you did.
>It will greatly help us to integrate your changes! 

### Bug reports and feature requests
If you encounter a bug, or have an idea for a new feature, please fill an [issue](https://github.com/shapeforge/Chill/issues) so we can discuss about it.
>**Note**
>Please be as precise as possible when filling an issue. For bug reports, please join some scripts/files that reproduce the problem.
>Using a label on your Issue will greatly help us tracking and processing them.

### C++ Style Guide
You can follow the [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html) for new code.

# Credits
## Developpers:

- Jimmy Etienne [[@JuDePom](https://github.com/JuDePom)] 
- Pierre Bedell [[@Phazon54](https://github.com/Phazon54)] 
- Thibault Tricard [[@ThibaultTricard](https://github.com/ThibaultTricard)] 
- Cedric Zanni [[@czanni](https://github.com/czanni)] 

## Logos:

- Pierre-Alexandre Hugron [[@pa_hugron](https://www.instagram.com/pa_hugron/)] 

## Acknowledgments:

Special thanks to the [IceSL devs](https://icesl.loria.fr/about/) and in particular Salim Perchy [[@ysperchy](https://github.com/ysperchy)] for his help!

ChiLL initial development was supervised by Sylvain Lefebvre [[@sylefeb](https://github.com/sylefeb)]. 
It is inspired by an earlier prototype by Jean Hergel [[@jhergel](https://github.com/jhergel)]. 

Feel free to join us in improving ChiLL!

## External libraries and tools used:

- [dear imgui](https://github.com/ocornut/imgui)
- [LibSL](https://github.com/sylefeb/LibSL)
- [lua5.1](https://www.lua.org/versions.html)
- [luabind-deboostified](https://github.com/decimad/luabind-deboostified)
- [tinyfiledialogs](https://github.com/native-toolkit/tinyfiledialogs)

## Funding:

ChiLL initial development was mainly supported by the ERC ShapeForge (StG-2012-307877) and [Inria](https://www.inria.fr/en/).

[//]: # (Ressources)
[banner]: ressources/images/banner/chill_banner_wide_medium.png
[node_menu]: ressources/images/guide/nodemenu.gif
[input_node]: ressources/images/guide/inputnode.gif
[linking_nodes]: ressources/images/guide/linknode.gif
[live_preview]: ressources/images/guide/preview.gif

[//]: # (Release links)
[win_zip]: https://github.com/shapeforge/Chill/releases/download/0.1.2/chill_0.1.2_win64.zip
[linux_zip]: https://github.com/shapeforge/Chill/releases/download/0.1.2/chill_0.1.2-0_amd64.tar.gz
[win_msi]: https://github.com/shapeforge/Chill/releases/download/0.1.2/Chill_Installer.msi
[deb_install]: https://github.com/shapeforge/Chill/releases/download/0.1.2/chill_0.1.2-0_amd64.deb

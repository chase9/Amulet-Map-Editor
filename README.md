# Amulet Map Editor

![Build](../../workflows/Build/badge.svg)
![Unittests](../../workflows/Unittests/badge.svg?event=push)
![Stylecheck](../../workflows/Stylecheck/badge.svg?event=push)
[![Documentation Status](https://readthedocs.org/projects/amulet-map-editor/badge)](https://amulet-map-editor.readthedocs.io)

A new Minecraft world editor and converter that supports all versions since Java 1.12 and Bedrock 1.7.

![edit](resource/img/edit.jpg)

## Running compiled builds

Download the zip file for your operating system from the list of [compiled builds](https://github.com/Amulet-Team/Amulet-Map-Editor/releases). (Currently Windows only)

Extract the contained folder to a location on your computer and run the executable.

## Running from Source

**If you are running a compiled build you do NOT need to do this.**

### 1. Install Dependencies

#### Fedora
```bash
sudo dnf install freeglut-devel git
```

#### Ubuntu
```bash
sudo apt-get install freeglut3-dev git
```

### 2. Clone Repository
```bash
git clone https://github.com/Amulet-Team/Amulet-Map-Editor.git
cd Amulet-Map-Editor
```

### 3. Build Amulet Map Editor
```bash
python3 -m venv .venv && source .venv/bin/activate   # (Optional) Set up a virtual environment
python3 -m pip install wxPython --no-cache-dir       # This step can take a long time
python3 -m pip install -e .
```

### 4. Run Amulet Map Editor
```bash
python3 -m amulet_map_editor
```

### Notes

If you have python 2 installed `python` may point to the wrong version in which case you will have to swap out `python` for `python3`

When installing from source the following dependencies will be installed

- numpy
- wxpython
- pyopengl
- [Amulet-Core](https://github.com/Amulet-Team/Amulet-Core)  The library to handle loading and saving data to the world formats.
- [Amulet-NBT](https://github.com/Amulet-Team/Amulet-NBT)  The library to handle reading and saving NBT and SNBT.
- [PyMCTranslate](https://github.com/gentlegiantJGC/PyMCTranslate)  The library to handle block, block entity, entity and biome translation. between versions
- [Minecraft-Model-Reader](https://github.com/gentlegiantJGC/Minecraft-Model-Reader)  The library to handle loading block models and textures from a resource pack for use in the renderer.

## Contributing

For information about contributing to this project, please read the [contribution](contributing.md) file.

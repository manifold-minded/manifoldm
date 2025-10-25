# ManifoldM

A collection of PySide6-based tools designed for Autodesk Maya workflows with an intuitive user interface. (Work in progress)

## Tools Included
- Orienter: interactively orient joints with control over Aim/Up axes, world-up
  direction, auto-orient secondary axis, manual tweaks and
  visibility control for selected or all joints in the scene.
- Colorizer: apply viewport override index colors to selected shape
  nodes, and mesh id color vertex generator.

## Requirements
- Autodesk Maya 2025 or later.

## Installation

1. [Click Here to Download ManifoldM](https://github.com/manifoldmindedmendit/manifoldm/releases/download/v0.1.0/manifoldm-0.1.0.zip)
2. Extract the contents to:
    - Windows: "C:/Users/{username}/maya/scripts/"
    - macOS: "/Users/{username}/Library/Preferences/Autodesk/maya/scripts/"
    - Linux: "/home/{username}/maya/scripts/"
3. In userSetup.mel, add the following line:

```mel
python("import manifoldm_loader");
```

## Usage (inside Maya)
By default, the menu ManifoldM will be added to the main Maya menu.

You can also add the following snippets to a Maya shelf button for quick access:

```python
from tools.orienter import OrienterWidget; OrienterWidget.show_dialog()

from tools.colorizer import ColorizerWidget; ColorizerWidget.show_dialog()
```

Alternatively, pressing Shift+Right-Click on the selected toolbar will create a new shelf button for each tool.


## Notes
 
- These tools are only compatible with Maya 2025/2026 as there are maya.cmds functions that are not available
  in earlier versions. PySide2 is also not supported to ensure future versions compatibility.

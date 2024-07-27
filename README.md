# Add-on Template for Blender 4.2

This is a basic template for creating add-ons for Blender 4.2. It includes essential files and a basic structure to help you get started quickly.

## File Structure

```
addon_template_4_2/
├── .gitignore
├── build.bat
├── LICENSE
├── README.md
└── source/
    ├── blender_manifest.toml
    └── __init__.py
```

### build.bat
A batch script to build the add-on into a ZIP file for distribution. It runs the following command:

```bat
"C:\Program Files\Blender Foundation\Blender 4.2\blender.exe" -c extension build --source-dir=./source
```

### source/
Contains the main code and metadata for the add-on.

- **blender_manifest.toml**: Defines the add-on's metadata including ID, version, name, description, maintainer, compatible Blender versions, and more.

  Example content:
  ```toml
  schema_version = "1.0.0"

  id = "addon_name_id"
  version = "1.0.0"
  name = "Add-on Name"
  tagline = "A short description of the add-on."
  maintainer = "Maintainer Name <email>"
  type = "add-on"

  website = "https://example.com or GitHub repository"

  tags = [
    "Node", "Pipeline", "User Interface"
  ]

  blender_version_min = "4.2.0"

  license = [
    "SPDX:GPL-3.0-or-later",
  ]

  copyright = [
    "2024, Maintainer Name",
  ]
  ```

- **\_\_init\_\_.py**: The main script file for the add-on. This file is executed when the add-on is loaded into Blender.

## Building the Add-on

To build the add-on into a ZIP file, run the `build.bat` script. This will package the contents of the `source/` directory into a ZIP file that can be installed in Blender.
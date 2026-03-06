# 🎬 EasyAnimation - Professional Animation Workbench for FreeCAD

![EasyAnimation Logo](icons/play.svg)

EasyAnimation is a powerful, beginner-friendly animation workbench for FreeCAD that allows you to create complex animations without writing a single line of code. Create mechanical animations, product demonstrations, and educational content with ease.

## 🌟 Features

### Core Features
- **Multi-Object Animation**: Animate multiple objects simultaneously
- **Keyframe System**: Position, Rotation, Scale, and Visibility keyframes
- **Visual Timeline**: Interactive timeline editor with keyframe markers
- **Real-time Playback**: Play, pause, stop with speed control
- **Loop Animation**: Seamless loop playback
- **Frame Export**: Export animations as PNG sequences

### Animation Types
- **Translation Animation**: Move objects from point A to B
- **Rotation Animation**: Rotate objects around any axis
- **Path Animation**: Make objects follow custom paths
- **Oscillation Animation**: Create back-and-forth motion
- **Scale Animation**: Scale objects over time (coming soon)

### Professional Features
- Multiple interpolation types (Linear, Bezier, Ease In/Out)
- Visual timeline with color-coded keyframes
- Object selection with checkboxes
- Frame-accurate positioning
- Speed control (0.25x to 8x)
- Project save/load

## 📋 Requirements

- FreeCAD 0.20 or higher
- Python 3.8+
- PySide2/Qt5 (included with FreeCAD)

## 🚀 Installation

### Automatic Installation (Recommended)
1. Open FreeCAD
2. Go to **Tools → Addon Manager**
3. Search for "EasyAnimation"
4. Click Install

### Manual Installation
1. **Locate your FreeCAD Mod directory:**
   - **Linux**: `~/.local/share/FreeCAD/Mod/`
   - **Windows**: `C:\Users\<username>\AppData\Roaming\FreeCAD\Mod\`
   - **macOS**: `~/Library/Application Support/FreeCAD/Mod/`

2. **Create the EasyAnimation folder:**
   ```bash
   cd /path/to/FreeCAD/Mod/
   mkdir EasyAnimation

Copy all files:
bash

# Clone or download the repository
git clone https://github.com/yourusername/EasyAnimation.git
cp -r EasyAnimation/* /path/to/FreeCAD/Mod/EasyAnimation/

    Restart FreeCAD

    Select the workbench:

        Click on the workbench dropdown

        Choose "EasyAnimation"

📖 User Guide
Quick Start - 5 Minute Tutorial
Step 1: Create or Open a Model

    Create a new document or open an existing one

    Make sure you have some objects to animate

Step 2: Select Objects to Animate

    In the EasyAnimation panel, find the "Objects to Animate" section

    Check the boxes next to objects you want to animate

    Use "Select All" to animate everything

Step 3: Add Keyframes

    Move the timeline slider to frame 0

    Click "Add Keyframe at Current Frame"

    Choose properties to keyframe (Position, Rotation, etc.)

    Move slider to frame 100

    Move/rotate your object to new position

    Click "Add Keyframe" again

Step 4: Play Animation

    Click the Play button (▶)

    Adjust speed using the dropdown

    Toggle Loop for continuous playback

Advanced Features
Creating a Path Animation

    Select your objects

    Click "Path" in Animation Presets

    Objects will follow a circular path

    Adjust duration in the timeline

Creating Rotation Animation

    Select objects

    Click "Rotate"

    Creates 360° rotation over 100 frames

    Modify keyframes for custom angles

Exporting Frames

    Click "Export Frames"

    Choose output directory

    Frames save as frame_0001.png, frame_0002.png, etc.

    Use external software to compile video

Timeline Controls

    Frame Slider: Drag to navigate frames

    Play/Pause/Stop: Control playback

    Speed: 0.25x to 8x playback speed

    Loop: Toggle continuous playback

    Current Frame Display: Shows frame number and time

Keyframe Colors

Keyframes are color-coded by property:

    🟢 Green: Position keyframes

    🔵 Blue: Rotation keyframes

    🟠 Orange: Scale keyframes

    🟣 Purple: Visibility keyframes

🏗️ Architecture
text

EasyAnimation/
├── __init__.py           # Package initialization
├── Init.py               # FreeCAD workbench init
├── InitGui.py            # GUI initialization
├── package.xml           # Package metadata
├── commands/             # Command modules
│   ├── __init__.py
│   ├── keyframe_commands.py
│   ├── playback_commands.py
│   └── export_commands.py
├── core/                 # Core animation logic
│   ├── __init__.py
│   ├── animation_engine.py
│   ├── timeline.py
│   ├── keyframe.py
│   └── interpolator.py
├── gui/                  # GUI components
│   ├── __init__.py
│   ├── main_panel.py
│   ├── timeline_widget.py
│   ├── keyframe_editor.py
│   └── object_list.py
├── icons/                # SVG icons
└── resources/            # Stylesheets
    └── styles.qss

🤝 Contributing

We welcome contributions! Here's how you can help:
Development Setup

    Fork the repository

    Clone your fork:
    bash

git clone https://github.com/yourusername/EasyAnimation.git

Create a symlink to FreeCAD Mod directory:
bash

ln -s /path/to/EasyAnimation ~/.local/share/FreeCAD/Mod/

    Make your changes

    Test thoroughly in FreeCAD

    Submit a Pull Request

Contribution Ideas

    New Animation Types: Add pendulum, spring, or wave animations

    Video Export: Implement direct MP4/AVI export

    Camera Animation: Animate camera views

    Physics Simulation: Add basic physics (gravity, collisions)

    Inverse Kinematics: For robotic animations

    Motion Capture: Import motion capture data

    Timeline Improvements: Drag-and-drop keyframes

    Graph Editor: Visual curve editing

    Particle Systems: For effects

    Documentation: Improve guides and examples

Coding Standards

    Follow PEP 8 style guide

    Add docstrings for all classes and methods

    Include comments for complex logic

    Use type hints where possible

    Test with multiple FreeCAD versions

Pull Request Process

    Update README.md with details of changes

    Update version numbers in relevant files

    Ensure all tests pass

    Get review from maintainers

    Squash commits if needed

🐛 Bug Reports

Found a bug? Please include:

    FreeCAD version

    EasyAnimation version

    Steps to reproduce

    Expected behavior

    Actual behavior

    Screenshots if applicable

    Error messages from Report View

📝 License

This project is licensed under the MIT License - see the LICENSE file for details.
🙏 Acknowledgments

    FreeCAD community for inspiration

    All contributors and testers

    Open source animation tools that inspired features

📞 Support

    GitHub Issues: Report bugs

    Forum: FreeCAD Forum thread

    Email: your.email@example.com

🎯 Roadmap
Version 1.1 (Coming Soon)

    Video export (MP4, AVI)

    Camera animation

    Graph editor for curves

    Undo/Redo support

Version 1.2 (Planned)

    Inverse kinematics

    Physics simulation

    Motion capture import

    Timeline copy/paste

Version 2.0 (Future)

    Particle systems

    Character animation

    Real-time rendering preview

    Network rendering

⚡ Quick Tips

    Use "Select All" to apply animations to multiple objects at once

    Keyframe at least 2 frames for smooth animation

    Export frames to create videos with external tools

    Use different interpolation for natural motion

    Save your timeline with File → Export Animation

    Check Report View for errors and messages

🎓 Examples
Example 1: Rotating Gear

    Import or create a gear

    Select it in object list

    Click "Rotate" preset

    Play animation

    Adjust speed as needed

Example 2: Sliding Piston

    Create cylinder and piston

    Select piston object

    Click "Translate"

    Set start and end positions

    Play to see piston move

Example 3: Planetary System

    Create sun and planets

    Select all planets

    Click "Path" for circular orbits

    Adjust individual keyframes for different speeds

    Add rotation for moons

Made with ❤️ for the FreeCAD community

Report Bug · Request Feature · Star on GitHub



## Additional Files to Create

### Create a `LICENSE` file (MIT License)

```txt
MIT License

Copyright (c) 2024 EasyAnimation Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Create a CONTRIBUTING.md file
markdown

# Contributing to EasyAnimation

First off, thank you for considering contributing to EasyAnimation! It's people like you that make EasyAnimation such a great tool.

## Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct: be respectful, inclusive, and constructive.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the issue list to avoid duplicates. When you create a bug report, include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the bug**
- **Provide specific examples** (screenshots, error messages)
- **Describe the behavior you observed vs expected**
- **Include your FreeCAD version and OS**

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

- **Use a clear and descriptive title**
- **Provide a step-by-step description** of the suggested enhancement
- **Provide specific examples** of how it would work
- **Explain why this enhancement would be useful**

### Pull Requests

1. **Fork the repo** and create your branch from `main`
2. **If you've added code that should be tested, add tests**
3. **Ensure your code follows our style guide**
4. **Update documentation** as needed
5. **Make sure your code lints**
6. **Submit the pull request**

## Development Process

### Setting Up Development Environment

1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/yourusername/EasyAnimation.git

Create a symlink to your FreeCAD Mod directory:
bash

ln -s $(pwd)/EasyAnimation ~/.local/share/FreeCAD/Mod/

    Make your changes

    Test in FreeCAD

Coding Style

    Follow PEP 8

    Use 4 spaces for indentation

    Maximum line length: 79 characters

    Use descriptive variable names

    Add docstrings for all public methods

    Comment complex logic

Testing

    Test all changes in FreeCAD

    Check the Report View for errors

    Test with multiple FreeCAD versions if possible

    Verify backward compatibility

Git Commit Messages

    Use the present tense ("Add feature" not "Added feature")

    Use the imperative mood ("Move cursor to..." not "Moves cursor to...")

    Limit the first line to 72 characters

    Reference issues and pull requests after the first line

Project Structure
text

EasyAnimation/
├── commands/          # FreeCAD commands
├── core/              # Core animation logic
├── gui/               # UI components
├── icons/             # SVG icons
├── resources/         # Stylesheets, translations
├── tests/             # Unit tests
├── Init.py           # Workbench init
├── InitGui.py        # GUI init
└── package.xml       # Package metadata

Adding New Features
Adding a New Animation Type

    Create new command in commands/

    Add logic in core/animation_engine.py

    Add UI control in gui/main_panel.py

    Add icon in icons/

    Register command in InitGui.py

Adding a New UI Component

    Create widget in gui/

    Add to main panel layout

    Connect signals/slots

    Update styles in resources/styles.qss

Release Process

    Update version in __init__.py

    Update package.xml

    Update CHANGELOG.md

    Create a GitHub release

    Tag version

Questions?

Feel free to contact the maintainers:

    Open an issue

    Post on FreeCAD forum

    Email: your.email@example.com

Thank you for contributing! 🎉
text


### Create `CHANGELOG.md`

```markdown
# Changelog

## [1.0.0] - 2024-01-15

### Added
- Initial release
- Multi-object animation support
- Keyframe system (Position, Rotation, Visibility)
- Visual timeline editor
- Playback controls with speed adjustment
- Loop animation
- Frame export as PNG
- Animation presets (Translate, Rotate, Path, Oscillate)
- Object selection with checkboxes
- Professional UI with stylesheets
- Package.xml for FreeCAD 0.20+

### Fixed
- Import issues with module structure
- Timeline update on frame change
- Multi-object keyframe handling

## [0.9.0] - 2023-12-01

### Added
- Beta release
- Basic animation engine
- Single object animation
- Keyframe support


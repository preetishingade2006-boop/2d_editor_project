# ASCII 2D Graphics Editor

A simple console-based 2D Graphics Editor written in C that allows users to create and display geometric shapes on an ASCII canvas. This project demonstrates fundamental computer graphics concepts, object management, and drawing algorithms using a terminal-based interface.

## Features

- Draw geometric shapes on an 80×24 ASCII canvas
- Support for multiple shape types:
  - Line
  - Rectangle
  - Circle
  - Triangle
- Store and manage multiple objects
- Delete objects from the scene
- Render all stored objects on demand
- Boundary-safe pixel plotting
- Midpoint Circle Algorithm implementation
- Object-oriented design using structures and unions

## Canvas Specifications

- Canvas Width: 80 characters
- Canvas Height: 24 characters
- Empty Pixel Character: `_`
- Drawn Pixel Character: `*`
- Maximum Objects: 100

## Supported Shapes

### Line
Defined by two endpoints:

(x1, y1) → (x2, y2)

Uses a DDA-style line drawing algorithm.

### Rectangle
Defined by:
- Top-left corner (x1, y1)
- Bottom-right corner (x2, y2)

Rendered using four connected lines.

### Circle
Defined by:
- Center point (cx, cy)
- Radius

Rendered using the Midpoint Circle Algorithm with 8-way symmetry.

### Triangle
Defined by three vertices:

(x1, y1)

(x2, y2)

(x3, y3)

Rendered by connecting the vertices with lines.

## Menu Options

When the program starts, the following menu is displayed:

1. Add object
2. Delete object
3. Modify object
4. Display picture
5. List objects
0. Exit

### Add Object
Create and store a new shape in the scene.

### Delete Object
Remove an object from the scene by its index.

### Modify Object
Reserved for future implementation.

### Display Picture
Render and display all valid objects on the canvas.

### List Objects
Reserved for future implementation.

## Compilation

Compile the program using GCC:

```bash
gcc graphics_editor.c -o graphics_editor

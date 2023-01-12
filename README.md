# SGDraw
SGDraw: Scene Graph Drawing interface

Our introductory video is [here](https://www.youtube.com/watch?v=acy0SNLfahg&lc=UgyolK17UbvOUGuEFE94AaABAg)

>Functions

**Removing.** The design of the removing function is based on the concept of tree construction, and the removing operation is implemented with the commonly used backspace key. Users are allowed to select any connection line for deletion, so as to divide the whole tree structure into several subtrees. Users can also select a node to delete, both the selected node and its subtrees will be deleted at the same time.

**Cloning.** The design of the cloning function is still based on the tree structure. When users select a node, its subtree will also be selected and copied, so as to ensure that the attributes and relationships corresponding to the object can also be copied. The function keys are designed as "Ctrl", "C", and "V". "Ctrl + C" to realize the copy function, and "Ctrl + V" to realize the paste function. This is consistent with people's usual habits, so it will not bring operation trouble to users.

**Undo.** We design the Undo function. This function is implemented based on "Ctrl" and "Z". It allows users to go back to the previous scene graph state. Users can go back until all operations disappear. This will reduce the users' error cost and simplify the modification process.

**Zoom and Collapsing.** Scene graphs will get large for complex images. One way to simplify the scene graphs is to hide the branches of the tree. "Collapsing" a node means making all of its children and the links to them, not visible, and recursively collapsing all of the children that have children. The other operation is zoom in/zoom out, the SGDraw allows users to use the mouse wheel to zoom in or zoom out the scene graphs, which supports users to draw more scene graphs in a limited drawing area.

**Dragging.** We provide users with a tree layout to display the scene graphs hierarchically on the interface. Users are allowed to modify the default layout by dragging nodes or edges.



# SGDraw
SGDraw: Scene Graph Drawing interface


**Removing.** The design of the removing function is based on the concept of tree construction, and the removing operation is implemented with the commonly used backspace key. Users are allowed to select any connection line for deletion, so as to divide the whole tree structure into several subtrees. Users can also select a node to delete, both the selected node and its subtrees will be deleted at the same time.

**Cloning.** After creating an object with its corresponding attributes and relationships, users can quickly complete the construction of the same object through the cloning function and small modifications. This function reduces the pressure on users with complex image processing, and also increases the efficiency of the SGDraw in processing complex images. The design of the cloning function is still based on the tree structure. When users select a node, its subtree will also be selected and copied, so as to ensure that the attributes and relationships corresponding to the object can also be copied. The function keys are designed as ``Ctrl'', ``C'', and ``V''. ``Ctrl + C'' to realize the copy function, and ``Ctrl + V'' to realize the paste function. This is consistent with people's usual habits, so it will not bring operation trouble to users.

**Undo.** As a time-consuming task, it is difficult to modify the scene graphs in the previous interfaces. After errors are found, it is necessary to delete the content and input it again. To simplify the users' operation, we design the Undo function. This function is implemented based on ``Ctrl'' and ``Z''. It allows users to go back to the previous scene graph state. Users can go back until all operations disappear. This will reduce the users' error cost and simplify the modification process.

**Zoom and Collapsing.** Scene graphs will get large for complex images. One way to simplify the scene graphs is to hide the branches of the tree. ``Collapsing" a node means making all of its children and the links to them, not visible, and recursively collapsing all of the children that have children. The other operation is zoom in/zoom out, the SGDraw allows users to use the mouse wheel to zoom in or zoom out the scene graphs, which supports users to draw more scene graphs in a limited drawing area.

**Dragging.** The layout is an important cornerstone in graph visualization. A reasonable layout of scene graphs can help users quickly analyze results and accurately locate issues. The unreasonable layout of the scene graphs, such as GeneAnnotation~\cite{zhang2021geneannotator}, is difficult for users to extract the desired information from the graphs. We provide users with a tree layout to display the scene graphs hierarchically on the interface. Users are allowed to modify the default layout by dragging nodes or edges.



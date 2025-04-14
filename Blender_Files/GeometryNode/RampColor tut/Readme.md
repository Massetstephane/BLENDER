## how to control all parameter in color Ramp Converter node

the complete node :
![](https://github.com/Massetstephane/BLENDER/blob/2c3461362b2ee1040f2bdde2c2f4113735dcf6cf/Render/Ramp-PIctures/global-node.jpg)

### the template added as example : 

- with 4 position and color named 'Color 1', 'color 2'.. for color and for position 'Color 1 Position', 'Color 2 Position'..
- name of the position is very important for the drivers using the correct label and not the interne python data (ex : data["Color 4 Position"])

![](https://github.com/Massetstephane/BLENDER/blob/e2bc90024730b6b9eda03975a0c71dba581c03fe/Render/Ramp-PIctures/base-colorRamp.jpg)

## MAIN node ungrouped (Ramp test)

![](https://github.com/Massetstephane/BLENDER/blob/e90c3807a2435c1e956345adf4c52a429098a07b/Render/Ramp-PIctures/Ramp-test-ungrouped.jpg)

- Group Input collecte all colors and 'Color # Position' are not used
- if you add new input here, driver is broken because order change in python if you keep the info copied same as internal.
- Color are passed throught c1, c2.. in Ramp group.

## RAMP group (drivers for color position in this group)

![](https://github.com/Massetstephane/BLENDER/blob/eff1deeb6bab1e3ea771f50d03686af8743bdc8a/Render/Ramp-PIctures/Ramp-ungrouped.jpg)

- below the nodes the ramp color template (frame) using for this example is inactive.
- see the Ryan King Art tutorial for the how to !

## Inside driver

![](https://github.com/Massetstephane/BLENDER/blob/0ce7654d8b3d3b005ffae5018dd14cbf7a7bc426/Render/Ramp-PIctures/drivers.jpg)

- paste the drivers in path give :  node_tree.nodes["GroupBase"].inputs[6].default_value
- .inputs[6] is the index (6) for the slot 'color 1 Position' in Group Input and if you change the order or add new input index change and driver take bad index.
- But (see above) if the label slot is used : .inputs["Color 1 Position"] driver work if you change something in Group Input later.


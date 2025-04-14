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

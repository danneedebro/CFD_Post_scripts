# CFD_Post_scripts
Ansys CFD Post Script

## ```void listParameters(Object Name,[Indent Level])```
Writes out all parameters and their values of an object (and their children) to console.

### Example
```
listParameters("/VIEW: Figure 1/CAMERA")
```
Prints out all parameters and their values for the (singleton) camera object in "Figure 1".

**Output:**
```
CAMERA:CAMERA
   Option = Pivot Point and Quaternion
   Pan = 0,0
   Pivot Point = 0,0,0
   Rotation = -90, 0, 0
   Rotation Quaternion = 0.279848,-0.364705,-0.115917,0.880476
   Scale = 1
   Send To Viewer = True
END
```
### Example
```
listParameters("/VIEW: Figure 1/CAMERA", 1)
```
Does the same but with 1 level of indentation
**Output:**
```
   CAMERA:CAMERA
      Option = Pivot Point and Quaternion
      Pan = 0,0
      Pivot Point = 0,0,0
      Rotation = -90, 0, 0
      Rotation Quaternion = 0.279848,-0.364705,-0.115917,0.880476
      Scale = 1
      Send To Viewer = True
   END
```


### Example
```
listParameters("/VIEW: Figure 1")
```
Lists all properties of Figure 1, also its child object CAMERA
**Output:**
```
VIEW: Figure 1
   Angular Coord Shift = 0.0
   Auto Center = false
   Axis Visibility = On
   Border Visibility = false
   Camera Mode = User Specified
   Clip Plane = 
   Clip Scene = false
   Coord Transform = Cartesian
   Hide Difference Case = false
   Highlight Type = Surface Mesh
   Is A Figure = true
   Light Angle = 50, 110
   Local Object List = 
   Object Visibility List = /DEFAULT LEGEND:Default Legend Figure 1,/WIREFRAME:Wireframe
   Projection = Orthographic
   Ruler Visibility = On
   Standard View = Isometric Y
   Valid Case = All Cases
   CAMERA:CAMERA
      Option = Pivot Point and Quaternion
      Pan = 0,0
      Pivot Point = 0,0,0
      Rotation = -90, 0, 0
      Rotation Quaternion = 0.279848,-0.364705,-0.115917,0.880476
      Scale = 1
      Send To Viewer = True
   END
END
```


## ```void setParameters(Object Name, Parameter, Value)```
Sets a parameter in an object

### Example
```
setParameters("/VIEW: Figure 1","Projection","Perspective")
```
Sets the projection of Figure 1 to Perspective.

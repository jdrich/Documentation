---
ID_PAGE: 25119
PG_TITLE: Camera
PG_VERSION: 2.1
TAGS:
    - Node
    - Camera
---
## Description

class [Camera](/classes/3.0/Camera) extends [Node](/classes/3.0/Node)



## Constructor

## new [Camera](/classes/3.0/Camera)(name, position, scene)

Creates a new [Camera](/classes/3.0/Camera).
A tutorial about [ArcRotateCamera](/classes/3.0/ArcRotateCamera) can be found here : https://doc.babylonjs.com/How_To/Cameras

#### Parameters
 | Name | Type | Description
---|---|---|---
 | name | string |      
 | position | [Vector3](/classes/3.0/Vector3) |      The camera position
 | scene | [Scene](/classes/3.0/Scene) |      The scene linked to this camera
## Members

### inputs : [CameraInputsManager](/classes/3.0/CameraInputsManager)&lt;[Camera](/classes/3.0/Camera)&gt;



### static PERSPECTIVE_CAMERA : number



### static ORTHOGRAPHIC_CAMERA : number



### static FOVMODE_VERTICAL_FIXED : number



### static FOVMODE_HORIZONTAL_FIXED : number



### static RIG_MODE_NONE : number



### static RIG_MODE_STEREOSCOPIC_ANAGLYPH : number



### static RIG_MODE_STEREOSCOPIC_SIDEBYSIDE_PARALLEL : number



### static RIG_MODE_STEREOSCOPIC_SIDEBYSIDE_CROSSEYED : number



### static RIG_MODE_STEREOSCOPIC_OVERUNDER : number



### static RIG_MODE_VR : number



### static RIG_MODE_WEBVR : number



### static ForceAttachControlToAlwaysPreventDefault : boolean



### position : [Vector3](/classes/3.0/Vector3)

Position of the camera

### upVector : [Vector3](/classes/3.0/Vector3)

[Camera](/classes/3.0/Camera) up

### orthoLeft : any

For orthographic camera, it's the left side of point of view

### orthoRight : any

For orthographic camera, it's the right side of point of view

### orthoBottom : any

For orthegraphic camera, it's the bottom side of point of view

### orthoTop : any

For orthographic camera, it's the top side of point of view

### fov : number

Field of view of the camera

### minZ : number

Minimum distance of view

### maxZ : number

Maximum distance of view

### inertia : number

Inertia of the camera

### mode : number

0 = PERSPECTIVE

1 = ORTHOGRAPHIC

### isIntermediate : boolean

True if this camera is a subcamera, false otherwise

### viewport : [Viewport](/classes/3.0/Viewport)

The viewport

### layerMask : number

The layerMask

### fovMode : number



### cameraRigMode : number



### interaxialDistance : number



### isStereoscopicSideBySide : boolean



### globalPosition : [Vector3](/classes/3.0/Vector3)



### rigCameras : [Camera](/classes/3.0/Camera)[]



### rigPostProcess : [PostProcess](/classes/3.0/PostProcess)



### leftCamera : [FreeCamera](/classes/3.0/FreeCamera)



### rightCamera : [FreeCamera](/classes/3.0/FreeCamera)



## Methods

### getClassName() &rarr; string


### toString(fullDetails) &rarr; string



#### Parameters
 | Name | Type | Description
---|---|---|---
optional | fullDetails | boolean |   

### getActiveMeshes() &rarr; [SmartArray](/classes/3.0/SmartArray)&lt;[Mesh](/classes/3.0/Mesh)&gt;


### isActiveMesh(mesh) &rarr; boolean



#### Parameters
 | Name | Type | Description
---|---|---|---
 | mesh | [Mesh](/classes/3.0/Mesh) |      

### attachControl(element, noPreventDefault) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | element | HTMLElement |      Element to detach control and display
optional | noPreventDefault | boolean |   
### detachControl(element) &rarr; void

Detach the control and display of the camera from the element

#### Parameters
 | Name | Type | Description
---|---|---|---
 | element | HTMLElement |      Element to detach control and display

### update() &rarr; void


### attachPostProcess(postProcess, insertAt) &rarr; number

Attaches a given post process

#### Parameters
 | Name | Type | Description
---|---|---|---
 | postProcess | [PostProcess](/classes/3.0/PostProcess) |      @param postProcess
optional | insertAt | number |      Index of postProcess to add
### detachPostProcess(postProcess, atIndices) &rarr; number[]

Detach a fiven post process

#### Parameters
 | Name | Type | Description
---|---|---|---
 | postProcess | [PostProcess](/classes/3.0/PostProcess) |      @param postProcess
optional | atIndices | any |      Index of postProcess to detach
### getWorldMatrix() &rarr; [Matrix](/classes/3.0/Matrix)

Get the worldMatrix
### getViewMatrix(force) &rarr; [Matrix](/classes/3.0/Matrix)

Get the viewMatrix

#### Parameters
 | Name | Type | Description
---|---|---|---
optional | force | boolean |      

### freezeProjectionMatrix(projection) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
optional | projection | [Matrix](/classes/3.0/Matrix) |  

### unfreezeProjectionMatrix() &rarr; void


### getProjectionMatrix(force) &rarr; [Matrix](/classes/3.0/Matrix)

Get the projectionMatrix

#### Parameters
 | Name | Type | Description
---|---|---|---
optional | force | boolean |      

### getTranformationMatrix() &rarr; [Matrix](/classes/3.0/Matrix)


### isInFrustum(target) &rarr; boolean



#### Parameters
 | Name | Type | Description
---|---|---|---
 | target | ICullable |  

### isCompletelyInFrustum(target) &rarr; boolean



#### Parameters
 | Name | Type | Description
---|---|---|---
 | target | ICullable |  

### getForwardRay(length, transform, origin) &rarr; [Ray](/classes/3.0/Ray)



#### Parameters
 | Name | Type | Description
---|---|---|---
optional | length | number | 
optional | transform | [Matrix](/classes/3.0/Matrix) | 
optional | origin | [Vector3](/classes/3.0/Vector3) | 
### dispose() &rarr; void


### getLeftTarget() &rarr; [Vector3](/classes/3.0/Vector3)


### getRightTarget() &rarr; [Vector3](/classes/3.0/Vector3)


### setCameraRigMode(mode, rigParams) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | mode | number |      
 | rigParams | any |      
### setCameraRigParameter(name, value) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | name | string |      
 | value | any |      
### createRigCamera(name, cameraIndex) &rarr; [Camera](/classes/3.0/Camera)

needs to be overridden by children so sub has required properties to be copied

#### Parameters
 | Name | Type | Description
---|---|---|---
 | name | string |      
 | cameraIndex | number |      
### serialize() &rarr; any


### clone(name) &rarr; [Camera](/classes/3.0/Camera)



#### Parameters
 | Name | Type | Description
---|---|---|---
 | name | string |      

### getDirection(localAxis) &rarr; [Vector3](/classes/3.0/Vector3)



#### Parameters
 | Name | Type | Description
---|---|---|---
 | localAxis | [Vector3](/classes/3.0/Vector3) |  

### getDirectionToRef(localAxis, result) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | localAxis | [Vector3](/classes/3.0/Vector3) |  
 | result | [Vector3](/classes/3.0/Vector3) |  
### static GetConstructorFromName(type, name, scene, interaxial_distance, isStereoscopicSideBySide) &rarr; () =&gt; [Camera](/classes/3.0/Camera)



#### Parameters
 | Name | Type | Description
---|---|---|---
 | type | string |   
 | name | string |      
 | scene | [Scene](/classes/3.0/Scene) |      The scene linked to this camera
optional | interaxial_distance | number |   
### static Parse(parsedCamera, scene) &rarr; [Camera](/classes/3.0/Camera)



#### Parameters
 | Name | Type | Description
---|---|---|---
 | parsedCamera | any |    
 | scene | [Scene](/classes/3.0/Scene) |      The scene linked to this camera



Summary of the script:




 *************   Commands to run the blender file  **************


-->  For simplicity we added a comments where to add and what to add.
-->  Runninng this program is very easy in blender software
-->  Just downlaod the blender file and save in your System.
-->  Open the file in blender software and change the PATH in Code snippet to save the image dataset at that location.
-->  Click on RUN button and check the location where you assigned a path to save the images as DATASET.







********** Instructions to be followed for creating a blender model *************


--> Intially OPEN Script.py in blender software .
--> Upload the image in either .FBX, .OBJ format. ( Provided in the folder )
--> If necessary check the comment in code how to and where to add the image. 
--> Give the PATH properly to store the images as a dataset.
--> Save the file and reanme however you want to be and starting your script.


                  ***********  END  *********************



Basic points to be considered: 

--> We will create a simple scene with a plane, 3D model,texture, a light source, and a camera. 
--> Then I will show you how you can rotate a virtual camera around a model and use it to render from 3D to 2D from different viewpoints using the Blender API.
--> The first thing to do is to open Blender and click on the scripting tab. And Then click New.


-->

Importing blender Python,numpy packages

If we want to move the model, we can also do that with:

cube.location[0]+=10 



-->  create a light source in Blender using Python

-->  To see how powerful this light source is in Blender, we can render it:

--> The light source is of type POINT, which is similar to artificial light. To control the power of the light source, we set the intensity in watts:

light.data.energy=200.0

--> There are more types of lights. If you want a more powerful light, similar to the sun, instead of creating a light as of type POINT, we create a light as type SUN

-->  create a Camera in Blender using Python

--> Without a camera, it is not possible to render a scene from 3D to 2D. So let’s create a camera.

--> In this Code Snippet Eulers Fucntions Plays a major in roation of the camera around the source of 360 Degrees.

-->  We specify use_nodes=True to enable the node’s functionality in Blender:

mat.use_nodes=True

--> With nodes in Blender, you can create very complex materials, through the composition of multiple nodes in a tree that applies some operation on a material using a variety of inputs, which can be routed from one node to another. 

--> It is very powerful but also can get very complex. By default, a new material created in Blender comes with a Principled BSDF shader node and a Material Output node. 


--> To add a constraint to track an object using the camera is as simple as:

constraint = cam.constraints.new(type='TRACK_TO')
constraint.target= Image Name









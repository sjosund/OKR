# 3D-Aware Scene Manipulation via Inverse Graphics
##Summary
* Scene encoder performs inverse graphics, and translates a scene into a structured object-wise represenetation.
* Three branches
    * (1) Semantic de-renderer
        * Creates segmantic segmentation map. Uses Dilated ResNet.
    * (2) Geometric de-renderer
        * Uses Mask R-CNN to create an instance segmentation from which scale, rotation, translation, mesh model, and FFD coefficients are predicted. These can be manipulated in inference time. These parameters are sent into a 3D renderer
    * (3) Textural de-renderer
        * Based on the (1) and (2) each instance’s texture is encoded into a low-dimensional representation.
* Combining the output from (2) and (3) the textures are rendered to give the output. A GAN is used to inprove the photorealism of the outputs.
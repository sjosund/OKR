# Deep GrabCut for Object Selection
## Summary
- EncDec-segmentation model takes RGB image + “Distance from bounding box” channel and outputs a segmentation map
- The DBB-map is inside/outside aware.
- Rectangle sampling - They jitter the bounding boxes to generate more training data.
- They are doing some wighting based on the detection boxes. I’m not sure about the details on this.
- They use a CRF as a final label assignment step.
- Points of improvement
    - Uses a VGG16 encoder without any skip connections. Change to U-Net type model.


#Automatic Portrait Segmentation for Image Stylization
##Summary
* Builds model for portrait segmentation.
* First detects the face using some external(?) face detection algorithm.
* Crops the face.
* Adds a canonical face mask prior and transforms it into the cropped portrait using face landmarks.
* Adds “Normalized x and y”-masks, that have values depending on the distance from the center of the face.
* Feeds the masks and face crop to a FCN, that outputs a segmentation mask.
* Generates trimap by setting all pixels within a 10-pixel radius from the boundary to “unknown" region.
* Finally applies KNN-matting.

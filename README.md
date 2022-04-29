# Fashion-Recommendation-System
###TO RUN IMAGE SEARCHING :

streamlit run c:/Users/atlur/Downloads/Fashion-Image-Search-Engine-main/Fashion-Image-Search-Engine-main/FashionImgSearchEngine_Deployment.py 

###TO RUN TAILORING MECHANISM :

The aim of this functionality is to determine the body measurements of a person as accurately as possible from a set of given input images. In order to do that we need to have atleast one known length in the image.

We are using a checker board for the same. Checker board helps in calibration of camera image world for 3D measurements. If you use any other chess-type board, measure the side length of unit square and change global ref_ht parameter in code2.py. 

The repository includes methods to measure shoulder distance, wrist-to-shoulder measurement, and waist approximation. There are three input images

The repository includes methods to measure shoulder distance, wrist-to-shoulder measurement, and waist approximation. We require three input images to run the code.

Before running the code, make sure that you have all the required packages installed in your text editor.


The command for running the code (in the command is as follows):
python code2.py -i1 <path to Image1> -i2 <path to Image2> -i3 <path to Image3> -a <Correction_mode>

Correction_mode parameter is the flag, which tells code whether to perform affine + metric correction on the image. Enter True to perform correction else False

First 2 images that pops up is for finding waist circumference. Mark waist ends on both the image.
Next 2 images are for calculating shoulder length. Mark fall near neck both sides in first image and mark shoulder, both-sides in second image.

Repeat step 2 again. 
This is again calculating shoulder length for robustness from different image.

Mark both the wrist - end of hands nearly in the next popped image.

While in 2,3,4 points, there is also projected points shown. You can manually mark or not mark.
When code runs, you will be shown points selected by our heuristic as to-be shoulder/wrist. If suspicious/incorrect, you can explicitly select those points on image and pressing esc key thereafter.

###TO RUN VIRTUAL TRY ON :

Run the Python file : Flask.py

In order to try on more clothes : The dresses can be added into the same folder.

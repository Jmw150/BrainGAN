## Contributors
Prad Ejner, Dan Mohler, Jordan Winkler

## Dataset
Datasets are located on deepData/StudentData/sb_brain  
ArtUK was used for initial evaluation of model  
brain_tumor_mri_dataset contains images used for testing of various sizes  

## Output
Output files are located on deepData/StudentData/sb_brain/parameter_testing  
These contain model saves and generated images.  

## Models
art-gan.py was used to generate images from the ArtUK dataset  
brain-gan.py was used to generate images from mri-dataset with evaluation every 100 epochs  
brain-gan-parameter-search.py was used to generate images with varying parameters, with output only at the end  

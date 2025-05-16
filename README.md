# OIC-130_CellCountScript
This repository is for the analysis request from the Lien Lab to count cells automatically from images collected off the Incucyte microcope. Images are 8-bit grayscale brightfield, no fluorescence markers were used. 

Primary goal is to have as accurate of counts as possible; outline accuracy should be prioritized incase morphology metrics are desired later (not indicated at this time).

CellPose will be used for this segmentation task, but additional training is required.

Added in training from an additional 20 images with various levels of confluency. Transfer learning with the cyto3 model started to become overtrained on the brightfield data. Tested SGD and AdamW optimizers along with 100 and 200 epochs. Settled on IncucyteV4 model (20 additional labeled images, SGD, 100 epochs) with `diameter=20` as the best perfoming across low and high confluency images. Sent results to Sam for review.
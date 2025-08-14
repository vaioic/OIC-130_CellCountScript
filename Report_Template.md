# OIC-130 Cell Count

Total Hours: 5h

## Authorship and Methods

Research supported by the Optical Imaging Core should be acknowledged and considered for authorship. Please refer to our [SharePoint page](https://vanandelinstitute.sharepoint.com/sites/optical/SitePages/Acknowledgements-and-Authorship.aspx) for guidelines.

Please include our RRID in the methods section for any research supported by the OIC. RRID:SCR_021968

### Sample Acknowledgement

We thank the Van Andel Institute Optical Imaging Core (RRID:SCR_021968), especially [staff name], for their assistance with [technique/technology]. This research was supported in part by the Van Andel Institute Optical Imaging Core (RRID:SCR_021968) (Grand Rapids, MI).

## Summary of Request

Would like to optimize cell counting pipeline for data collected from the Incucyte.

## Brief summary of analysis pipeline

Trained a custom cellpose model to improve segmentation and counting of cells in bright field images. End results were not to the precision and accuracy desired; recommended using fluorescence imaging to improve results.

## Data

Bright field images collected from the Incucyte. Metadata not preserved in tif, unknown magnification, but likely 20X given relative size of cells in image.

![Example Image](/images/Example_BrightField.jpg)

## Analysis Pipeline

Trained a custom cellpose (v3.1.1) model based on ctyo3 to improve segmentation. Used the CellPose GUI with iterative training in where I manually annotated several images, trained a new model, assessed the performance and then added additional training until I reached the best performance I could with the data.

Examples of model performance:
![Example CellPose results](/images/CellPose_Output_Example.png)

Ran the best performing model [IncucyteV4](/model/IncucyteV4) on all data and sent results for review. Unfortunately, the accuracy and precision was not enough to move forward with, so this project was closed.

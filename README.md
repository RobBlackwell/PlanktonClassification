# PlanktonClassification
Models, code and example data

A combined effort by CEFAS, Plankton Analytics ltd. and the Turing Institute from a data Study Group in Dec. 2021 has resulted in a three category DNN model for plankton image sorting (derived by transfer learning a Resnet-50 CNN).

See https://github.com/alan-turing-institute/plankton-dsg-challenge

The images were collected using the Plankton Imager model 1 at a pixel resolution of 10 microns on board CEFAS RV Endeavour 2017-2020.

Scripts:
TorchExport.py reads a PyTorch (*.pth) model at 64bit double precision to Openvino (*.onnx) and reduced precision for faster classification
DNN_preSort.py offers a basic classification engine using the CopNonDetritus_42317_FP16 model. The model is embedded in the script.

A MAC laptop (2016 i7) runs the model and sorts the images in the predefined day sample/10-minute folder structure at a rate of about 30 images per second.
Each image has area and maj/min parameters extracted and saved to ./desc/DNN_reults.csv file


PUBLICATIONS
1. Pitois SG, et al. (2021) A first approach to build and test the Copepod Mean Size and Total Abundance (CMSTA) ecological indicator using in-situ size measurements from the Plankton Imager (PI). Ecological Indicators 123 (2021) 107307. https://doi.org/10.1016/j.ecolind.2020.107307
2. Pitois SG, et al. (2018). Comparison of a cost-effective integrated plankton sampling and imaging instrument with traditional systems for mesozooplankton sampling in the Celtic Sea. Front. Mar. Sci. 5, 5. https://doi.org/10.3389/fmars.2018.00005
3. Scott J, et al.  (2021) In situ automated imaging, using the Plankton Imager, captures temporal variations in mesozooplankton using the Celtic Sea as a case study. J. Plankton Research. https://doi.org/10.1093/plankt/fbab018.

The requirements.txt only contain the libraries needed for Yolo V1 and V2, as the other notebooks has code snippet to install their own required libraries.
Yolo V1 and V2 are trained on Kaggle, their notebook should be put on Kaggle to be used

Specifically:

YoloV1:
    Our yolov1 only used pretrained weight that can be import directly from pytorch, thus, no additional step need to be done.

YoloV2:
    After uploading the YoloV2 notebook to Kaggle, You'll need to upload 
    -"darknet_19_state.pt", name its model as "darknet-19"
    -"YoloV2.pt", name its model as "BestParams"
    -"V2/airplane" dataset, name its dataset as "gdit-0-1"
    You can have different names but if you do so you'll need to change their directory in the code.
    Run the cells in the notebook to retrain it, and the last cell would calculate the mAP (this may take a long time)
YoloV3-5-6-7-8:
    Simply upload their notebooks onto Google Colab and upload the "Dataset/Other" and the "Weights" folder to you google drive
    After mounting the drive, you should:
        - Change the directory to the mydataset.yaml and the pretrained weights in "Pretrained Weights" if you want to retrain
        - Change the path to the correct finetuned weights in ("Weights") and the path to the image you want to infer (It will also save the infered file to your drive, except v6, v6 will just show the infered image)
    Finally, running the cells in the notebook will install all necessary libraries, re-run the training and evaluation (Results will be save into your drive)

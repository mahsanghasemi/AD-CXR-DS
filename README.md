# AD-CXR-DS
 Anomaly Detection in Chest X-Rays Using Discrepancy Scores Within Bi-Allocation Model
1. requirements

    Python 3.6
    Pytorch 1.7.0
    tensorboard 2.5.0
    pillow 6.1.0
    pydicom 2.3.0 (for data preprocessing)

2. Download the training dataset of RSNA Pneumonia Detection Challenge 
3. run data/preprocess.py to preprocess  dataset . The output files should be *.png
4. transfer   the repartition files rsna_data.json to corresponding data roots and rename to data.json.
5. Train the reconstruction network for module A. 
python main.py --config cfgs/RSNA_AE.yaml --mode a
6. Train the reconstruction network for module B.
python main.py --config cfgs/RSNA_AE.yaml --mode b
 for evaluation :
python main.py --config cfgs/RSNA_AE.yaml --mode eval
python main.py --config cfgs/RSNA_AE.yaml --mode test

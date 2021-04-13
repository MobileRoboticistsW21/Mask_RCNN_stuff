# Mask_RCNN_with_flow
Download the Mask_RCNN_And_Optical_Flow.ipynb, then follow the cells to produce a .JSON file containing Mask RCNN bounding boxes and optical flows. 

This should be run BEFORE performing GM-PHD filter, as it provides the input for the filter.


# Evaluation
The evaluation kit used is provided in the MOT Chanllenge website  
Download the kit from here: https://github.com/dendorferpatrick/MOTChallengeEvalKit  
The evaluation kit needs a python version of 3.6.9 or newer but under 3.9 and MATLAB (we ran with R2020b).  

To run the evaluation, first need to setup the matlab python engine. Go to the matlab directory.  
`cd .\extern\engines\python` (in windows)  
`python setup.py install`

Then install the requirement package in the evaluation kit. Go to the direcotry of **MOTChallengeEvalKit-master**, run `pip install -r .\MOT\requirements.txt`

Then everything should be ready to go. We used dataset MOT16 training set MOT16-09 and MOT16-11 as the ground truth. Go to the data directory of **MOTChallengeEvalKit-master**, 
create a folder called MOT16 then put the MOT16-09 and MOT16-11 folder downloaded from https://motchallenge.net/data/MOT16/ in it. Then change the directory to .\MOTChallengeEvalKit-master\seqmaps, go to MOT16-train.txt, edit the content until there are only MOT16-09 and MOT16-11 left under name.

Use the function in json_to_txt.py to convert the json output file from PHD filter to txt file in a format that can be read by the evaualtion kit. Named the two results txt file to be MOT16-09.txt and MOT16-11.txt and put them in the directory .\MOTChallengeEvalKit-master\res\MOT16res  

In the .\MOTChallengeEvalKit-master directory, run `python .\MOT\evalMOT.py` and should get the evaluation metrics of MOTA, MOTP, etc.

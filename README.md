# DeepMEI
DeepMEI is a convolutional neural network based tool to identify non-reference MEIs in short-read sequencing data
<br/>
![This is an image](https://github.com/xuxif/DeepMEI/blob/main/workflow.png)
<br/>
### We highly recommend install the tool by bioconda:<br /><br />
1. Firstly, install the main script by bioconda:
```
conda install -c bioconda deepmei
```
2. Then, move additional data and models to the correct directory:
```
##2.1 find the right path where the deepmeiv1 installed,assuming you are in a deepmei environment:
which deepmeiv1
##Assume the directory is:~/software/DeepMEI-main/DeepMEI/deepmeiv1

##2.2 download and uncompress the file  from https://github.com/Kanglu123/deepmei_v1.0.0/blob/master/DeepMEI.tar.gz
tar -zxvf DeepMEI.tar.gz
##the additional data and models are in the directory DeepMEI

##2.3 copy data to the right path
cp -r ./DeepMEI/1000g_high_callset ~/software/DeepMEI-main/DeepMEI/DeepMEI/1000g_high_callset
cp -r ./DeepMEI/DeepMEI_model/referenc/* ~/software/DeepMEI-main/DeepMEI/DeepMEI/DeepMEI_model/reference
cp -r ./DeepMEI/DeepMEI_model/weights/* ~/software/DeepMEI-main/DeepMEI/DeepMEI/DeepMEI_model/weights
```
3. Test the tool:
```
deepmeiv1 -h
```
### note: 
At the initial completion, this tool will merge model files from DeepMEI/DeepMEI_model/weights/val_best_model/variables and generate a 200Mb consensus model file at the same directory.
Incomplete model file will cause error, so do not interrupt the pipeline when you first test it use a bam or a cram file.
### contact:
Please feel free to email to applykanglu@hotmail.com if you have any questions about how to use the tool.

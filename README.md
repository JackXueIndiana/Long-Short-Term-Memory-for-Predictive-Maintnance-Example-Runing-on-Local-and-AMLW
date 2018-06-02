# Long-Short-Term-Memory-for-Predictive-Maintnance-Example-Runing-on-Local-and-AMLW
This article shows you how to prepare and run the Deep learning algorithm from Microsfot CNTK to build a Long Short Term Memory (LSTM) model for auro-engine maintenance. The code is from Dr. Uz's post.

Dr. Uz published a blob on how LSTM can help resolving the predictive maintnace problem in 2017. Here is the link: https://azure.microsoft.com/en-us/blog/deep-learning-for-predictive-maintenance/
The Python notebook is at https://github.com/Azure/lstms_for_predictive_maintenance/blob/master/Deep%20Learning%20Basics%20for%20Predictive%20Maintenance.ipynb

As my learning process, I am trying to run her code on my PC on which Anaconda Python 3 has been installed. I also have Azure Machine Learning Workbench installed on the same PC.

To run on Anaconda Jupyter Notebook, I need to install two packages: keras and cntk. From a DOS prompt, you can run (assume pip has been isntalled) two commands:

pip install keras

pip install cntk

The dependencies and version required will be autommatically resolved by these two commands.

On Anaconda, by default, tenserflower will be the backend for Deep Learning Network (DLN) to switch to MIcrosoft Computer Network Toolkit (cntk), you need to update the keras cofig file.

In this location: C:\Users\<your root dir>\.keras, you will find a file keras.json. Open this file change the backend to cntk:

{
    "floatx": "float32",
    "epsilon": 1e-07,
    "backend": "cntk",
    "image_data_format": "channels_last"
}

In AMLW, you go from File > Open Command Prompt, then a DOS prompt will be opened and pointed to your AMLW installed folder. IN the DOS prompt, you can run the same commands:

pip install keras
pip install cntk

The good news is you don't need to change any config file, you will automatically get cntk as your DLN backend.



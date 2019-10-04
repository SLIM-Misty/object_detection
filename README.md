# object_detection
Tensorflow's object detection from models/research
From https://github.com/tensorflow/models/tree/master/research/object_detection:

1) Before following the 'models/research/object_detection' installation instructions, you will need to pip install tensorflow (pip install tensorflow-gpu if you have a GPU; pip install tensorflow if you don't).

2) Then, git clone the models/ repository [https://github.com/tensorflow/models] into your tensorflow dir, wherever that is located (if it's in an Anaconda environment, it will be within "anaconda3/envs/{env_name}/lib/python3.7{or whatever version you're using}/site-packages/".

3) After that, you can follow the 'models/research/object_detection' installation instructions, found here:
https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md.

4) If the installation test passes (python object_detection/builders/model_builder_test.py) then try to run the object_detection_tutorial.ipynb jupyter notebook. 

I ran into a deprecation error with tensorflow-gpu==2.0.0 on trying to run the basic installation test program.

With tensorflow-gpu==1.14.0 I passed the installation test, but I ran into this error in the tutorial notebook: "Could not create cudnn handle: CUDNN_STATUS_INTERNAL_ERROR" 
I solved it by "setting config.gpu_options.allow_growth = True", taken from this post [https://github.com/tensorflow/tensorflow/issues/24496]

For the exact way that I implemented this, check the edited notebook that I've posted to this repo. 

# Deep Learning AMI Developer Guide

-----
*****Copyright &copy; 2018 Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What Is the AWS Deep Learning AMI?](what-is-dlami.md)
   + [Example DLAMI Uses](examples.md)
   + [Features of the DLAMI](features.md)
+ [Getting Started](gs.md)
   + [Choosing Your DLAMI](options.md)
      + [Deep Learning AMI with Conda](overview-conda.md)
      + [Deep Learning Base AMI](overview-base.md)
      + [Deep Learning AMI with Source Code](overview-source.md)
      + [CUDA Installations and Framework Bindings](overview-cuda.md)
      + [DLAMI Operating System Options](overview-os.md)
   + [Selecting the Instance Type for DLAMI](instance-select.md)
      + [Recommended GPU Instances](gpu.md)
      + [Recommended CPU Instances](cpu.md)
      + [Pricing for the DLAMI](pricing.md)
+ [Launching and Configuring a DLAMI](launch-config.md)
   + [Step 1: Launch a DLAMI](launch.md)
   + [EC2 Console](launch-from-console.md)
   + [Marketplace Search](launch-from-marketplace.md)
   + [Step 2: Connect to the DLAMI](launch-config-connect.md)
   + [Step 3: Secure Your DLAMI Instance](launch-config-secure.md)
   + [Step 4: Test Your DLAMI](launch-config-test.md)
   + [Clean Up](launch-config-cleanup.md)
   + [Set up a Jupyter Notebook Server](setup-jupyter.md)
      + [Configure Jupyter Notebook on Your DLAMI](setup-jupyter-configure-server.md)
      + [Custom SSL and Server Configuration](setup-jupyter-config.md)
      + [Start the Jupyter notebook server](setup-jupyter-start-server.md)
      + [Configure the Client to Connect to the Jupyter Server](setup-jupyter-configure-client.md)
         + [Configure a Windows Client](setup-jupyter-configure-client-windows.md)
         + [Configure a Linux Client](setup-jupyter-configure-client-linux.md)
         + [Configure a MacOS Client](setup-jupyter-configure-client-mac.md)
      + [Test by Logging in to the Jupyter notebook server](setup-jupyter-login.md)
+ [Tutorials and Examples](tutorials.md)
   + [Using the Deep Learning AMI with Conda](tutorial-conda.md)
   + [Using the Deep Learning Base AMI](tutorial-base.md)
   + [Running Jupyter Notebook Tutorials](tutorial-jupyter.md)
   + [Apache MXNet](tutorial-mxnet.md)
   + [Caffe2](tutorial-caffe2.md)
   + [Chainer](tutorial-chainer.md)
   + [CNTK](tutorial-cntk.md)
   + [Keras](tutorial-keras.md)
   + [PyTorch](tutorial-pytorch.md)
   + [TensorFlow](tutorial-tensorflow.md)
   + [Theano](tutorial-theano.md)
   + [Running Model Server for Apache MXNet on the Deep Learning AMI with Conda](tutorial-mms.md)
   + [TensorFlow Serving](tutorial-tfserving.md)
   + [TensorBoard](tutorial-tensorboard.md)
   + [10 Minute Tutorials](tutorial-10min.md)
+ [Resources and Support](resources.md)
+ [Appendix](appendix.md)
   + [AMI Options](ami-options.md)
      + [Deep Learning AMI with Conda](conda.md)
      + [Deep Learning Base AMI](base.md)
      + [Deep Learning AMI with Source Code](source.md)
      + [Deep Learning AMI with CUDA 9](cuda9.md)
      + [Deep Learning AMI with CUDA 8](cuda8.md)
      + [AWS Deep Learning AMI, Ubuntu Versions](ubuntu.md)
      + [AWS Deep Learning AMI, Amazon Linux Versions](al.md)
      + [AWS Deep Learning AMI, Windows Versions](win.md)
   + [DLAMI: Release Notes](appendix-ami-release-notes.md)
      + [AWS Deep Learning AMI Release Archive](dlami-release-archive.md)
         + [AWS Deep Learning AMI Base Release Archive](dlami-release-archive-base.md)
            + [Release Note Details for Deep Learning Base AMI (Amazon Linux) Version 2.0](dlami-base-amazon-linux-latest.md)
            + [Release Note Details for Deep Learning Base AMI (Ubuntu) Version 2.0](dlami-base-ubuntu-latest.md)
            + [Release Note Details for Deep Learning Base AMI (Amazon Linux) Version 1.0](BASE_AML1.md)
            + [Release Note Details for Deep Learning Base AMI (Ubuntu) Version 1.0](BASE_UBUNTU1.md)
         + [AWS Deep Learning AMI Conda Release Archive](dlami-release-archive-conda.md)
            + [Release Note Details for Deep Learning AMI (Amazon Linux) Version 2.0](dlami-conda-amazon-linux-latest.md)
            + [Release Note Details for Deep Learning AMI (Ubuntu) Version 2.0](dlami-conda-ubuntu-latest.md)
            + [Release Note Details for Deep Learning AMI (Amazon Linux) Version 1.0](CONDA_AML1.md)
            + [Release Note Details for Deep Learning AMI (Ubuntu) Version 1.0](CONDA_UBUNTU1.md)
         + [AWS Deep Learning AMI Source Release Archive](dlami-release-archive-source.md)
            + [Deep Learning AMI with Source Code (CUDA 9, Ubuntu) Version: 2.0](dlami-source-ubuntu-latest.md)
            + [Deep Learning AMI Ubuntu Version: 2.4_Oct2017](Ubuntu2.4_Oct2017.md)
            + [Ubuntu DLAMI Release Archive](dlami-release-archive-ubuntu.md)
               + [Deep Learning CUDA 9 AMI Ubuntu Version: 1.0](CUDA9_Ubuntu1.md)
               + [Deep Learning AMI Ubuntu Version: 2.3_Sep2017](Ubuntu2.3_Sep2017.md)
               + [Deep Learning AMI Ubuntu Version: 2.2_August2017](Ubuntu2_2_August2017.md)
               + [Deep Learning AMI Ubuntu Version: 1.5_June2017](Ubuntu1_5_June2017.md)
               + [Deep Learning AMI Ubuntu Version: 1.4_June2017](Ubuntu1_4_June2017.md)
               + [Deep Learning AMI Ubuntu Version: 1.3_Apr2017](Ubuntu1_3_Apr2017.md)
               + [Deep Learning AMI Ubuntu Version: 1.2](Ubuntu1_2.md)
               + [Deep Learning AMI Ubuntu Version: 1.1](Ubuntu1_1.md)
               + [Deep Learning AMI Ubuntu Version: 1.0](Ubuntu1_0.md)
            + [Amazon Linux DLAMI Release Archive](dlami-release-archive-al.md)
               + [Deep Learning AMI with Source Code (CUDA 9, Amazon Linux) Version: 2.0](dlami-source-amazon-linux-latest.md)
               + [Deep Learning AMI Amazon Linux Version: 3.3_Oct2017](AML3.3_Oct2017.md)
               + [Deep Learning CUDA 9 AMI Amazon Linux Version: 1.0](CUDA9_AML1.md)
               + [Deep Learning AMI Amazon Linux Version: 3.1_Sep2017](AML3.1_Sep2017.md)
               + [Deep Learning AMI Amazon Linux Version: 2.3_June2017](AML2_3_June2017.md)
               + [Deep Learning AMI Amazon Linux Version: 2.2_June2017](AML2_2_June2017.md)
               + [Deep Learning AMI Amazon Linux Version: 2.1_Apr2017](AML2_1_Apr2017.md)
               + [Deep Learning AMI Amazon Linux Version: 2.0](AML2_0.md)
               + [Deep Learning AMI Amazon Linux Version: 1.5](AML1_5.md)
         + [AWS Deep Learning AMI Windows Release Archive](dlami-release-archive-windows.md)
            + [Release Note Details for Deep Learning AMI (Windows 2016) Version 1.0](WIN_2016.md)
            + [Release Note Details for Deep Learning AMI (Windows 2012 R2) Version 1.0](WIN_2012.md)
+ [Document History for AWS Deep Learning AMI Developer Guide](doc-history.md)
+ [AWS Glossary](glossary.md)
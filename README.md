# ML Notebooks / Experiments
This is where I am storing Colab notebooks I've written to learn about ML. 

* infini_gram.ipynb (Infini-gram)[https://arxiv.org/abs/2401.17377] with a small MLP  
* password_protection.ipynb is a small idea I've been messing with to see if I could create some sort of 'password protected' neural network.
* High level idea is that we create a new matrix P that poisons the neurons in some layer's weights W (by adding a huge scalar for eg). P is sparse and created based on a mask so that mask @ P = [0]
  We dedicate the first N dimensions in the input to the pasword and if the correct password is provided its converted into the mask that cancels out P. Otherwise, it does not cancel out P and so the poison matrix is applied.
  Right now it works but the P_mat doesn't actually have much effect on the predictions when it is applied (e.g. invalid password so the network should be broken).

Rest are self explanatory.


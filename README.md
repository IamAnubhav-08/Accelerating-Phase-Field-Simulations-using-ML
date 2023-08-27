# Accelerating-Phase-Field-Simulations-using-ML
An autoencoder+ConvLSTM model to predict microstructure evolution of binary alloys

Following is the workflow of the model - 
![Workflow](https://github.com/IamAnubhav-08/Accelerating-Phase-Field-Simulations-using-ML/assets/75220234/c0a3f05e-546c-4a5d-b7a9-6c8aca74549e)

# The Purpose -

In phase field calculations of an alloy exhibiting spinodal decomposition, the spatiotemporal evolution of the composition variable, ‘c’, is governed by the Cahn-Hilliard Equation. Phase-field modeling is done by making use of this equation and it is an effective tool to study the microstructure evolution for a particular alloy.

However, even though taking into account its highly accurate predictions, phase-field modeling itself is a computationally expensive tool that requires rigorous numerical solutions to differential equations to generate the microstructures. In this research study, we have restricted our study to a general double-well potential G vs. X curve that exhibits spinodal decomposition between its two inflection points. Our research is focused on building a machine learning model, which consists of an autoencoder along with a ConvLSTM for microstructure evolution prediction based on already generated frames from the phase-field modeling. In the initial study, we create a dataset from phase-field generated microstructures of 10 different compositions, consisting of 1000 images each. We train our machine-learning model using this dataset which will finally be able to predict the next ‘n’ frames of any unknown composition based on the previous ‘m’ frames.

Thus using this methodology, we can replace ‘n’ phase-field steps with our machine learning model which will significantly accelerate our
microstructure simulation and bring down the heavy computation cost.

# ML-for-FF-Pytorch

This is a machine learning project to get an optimized set of force-field (FF) parameters for lipid molecules for a molecular dynamics (MD) simulation, implemented using PyTorch Python library. The same project is implemented (in Python) without the use of PyTorch and the repository is named ML-for-FF. The FF parameters are based on thousands of MD simulation run where the lennard-jones (LJ) parameters and partial charges were changed for the lipid atoms and some experimental quantities were calculated for these MD simulation. The aim of this project is to train a neural-network with the experimental quantities as the input vector and the LJ parameters and the partial charges as the output vector. From this trained network, a set of LJ parameters and partial charges will be obtained, when the experimental quantities (to be precise, their values in in-vitro experiments) is an input vector. 

The code is optimized to be able to read the output files (example of the files are: fitness_0_14.txt and lipid_0_14.itp) generated by MD software package (gromacs) and extract the useful data to generate the input and output vectors for training the neural network. The input and output vectors are then fed to the neural network (written in the Network class) in order to optimise the biases and weights of the neurons. The 'trained' neural network, where the biases and weights are optimised, is tested to result in optimized set of LJ parameters and partial charges, when the input vector is a vector of the experimental quantities of the system. 

# Author

The program is written by <br/>
Swapnil Wagle <br/>
PhD Student, Dept. of Theory and Bioystems <br/>
Max Planck Institute of Colloids and Interfaces <br/> 
Potsdam, Germany <br/>
E-mail: swapnil.wagle[at]mpikg[dot]mpg[dot]de

# Reading Materials

For getting an idea about the MD simulations, neural networks and PyTorch, please refer to the following links:

MD simulations <br/>
Wikipedia read: https://en.wikipedia.org/wiki/Molecular_dynamics <br/>
Book by Michael P. Allen: https://udel.edu/~arthij/MD.pdf <br/>
Presentation by Prof. Dror, Stanford: https://web.stanford.edu/class/cs279/lectures/lecture4.pdf <br/>
Gromacs simulation package: http://www.gromacs.org <br/>

Neural networks <br/>
Wikipedia read: https://en.wikipedia.org/wiki/Artificial_neural_network <br/>
Introduction to feed forward neural network and back-propogation method:
https://skymind.ai/wiki/neural-network <br/>
An excellent and detailed description of the methods in feed forward neural networks (online book by Dr. Michael Nielsen):
http://neuralnetworksanddeeplearning.com

PyTorch <br/>
PyTorch website: https://pytorch.org <br/>
Neural Networks with PyTorch (Tutorial): https://pytorch.org/tutorials/beginner/blitz/neural_networks_tutorial.html <br/>
https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html <br/>
https://www.guru99.com/pytorch-tutorial.html <br/>



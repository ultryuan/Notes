# RANDO
Given the scope of multiple tracks, could be flight, sea or land, in a defined geographic area, with time stamped movement data. Without any guidelines, domain knowledge, and subject matter expertise, how to characterize this system to establish a normal such that any track's behaviour deviates from it, is considered an anomoly?

MSCRED is one such technique that characterizes track behaviours by building a signature matrix then ecode it with a CNN then train the model(missing info), then decode it back. The decoded SM is compared with the original SM, the difference serves as a measurement of deviation. 

# SIGNATURE MATRICES
MSCRED constructs signature matrices to characterize the system status in different time steps. (what is the system status?)
# CONVOLUTION ENCODER
As with computer vision, CNN is used here. A neural network of kernels is used to encode the inter correlations.
# ATTENTION BASED MODEL (RNN)?
The encoded matrices is then fed to this to capture temporal patterns. 
# DECONVOLUTION
decoder is used to reconstruct th einput signature
# LOSS FUNCTION
difference between reconstructed input signature and the original signature.

# THE MODEL
The parameters trained are the weights of the CNN and the deconvolutionary 

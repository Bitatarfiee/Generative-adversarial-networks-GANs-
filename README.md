# Generative-adversarial-networks-GANs-
generative model/discriminative model
The generator G is fed with random data from a latent space, and its role is to generate data resembling the real samples. In this example, you have a two-dimensional latent space, so that the generator is fed with random (z₁, z₂) pairs and is required to transform them so that they resemble the real samples.

The structure of the neural network G can be arbitrary, allowing you to use neural networks as a multilayer perceptron (MLP), a convolutional neural network (CNN), or any other structure as long as the dimensions of the input and output match the dimensions of the latent space and the real data.

The discriminator D is fed with either actual samples from the training dataset or generated samples provided by G. Its role is to estimate the probability that the input belongs to the actual dataset. The training is performed so that D outputs 1 when fed a real sample and 0 when it’s fed a generated sample.

As with G, you can choose an arbitrary neural network structure for D if it respects the necessary input and output dimensions. In this example, the input is two-dimensional. For a binary discriminator, the output may be a scalar ranging from 0 to 1.

The GAN training process consists of a two-player minimax game in which D is adapted to minimize the discrimination error between real and generated samples, and G is adapted to maximize the probability of D making a mistake.

Although the dataset containing the real data isn’t labeled, the training processes for D and G are supervised. At each step in the training, D and G have their parameters updated. In the original GAN proposal, the parameters of D are updated k times, while the parameters of G are updated only once for each training step. However, to simplify the training, you can consider k equal to 1.

To train D, at each iteration, you label some real samples taken from the training data as one and some generated samples provided by G as 0. This way, you can use a conventional supervised training framework to update the parameters of D to minimize a loss function,
# Dependencies
pytorch pytorch=1.4.0
matplotlib jupyter
# Files

# References


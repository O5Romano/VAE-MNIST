# VAE-MNIST
A CNN based VAE for MNIST
## Usage
After downloading the notebook and installing the necessary libraries, you should be able to execute the notebook. I recommend changing the epoch and max_step variables for less blurry results.<br/>
**plot_all_latent_dim()** – This function creates a "one-hot" vector for every latent dimension with a specific value. E.g., if latent_dim = 2 and value = 1, the function would generate the torch tensors [1, 0] and [0, 1].<br/>
It then passes them through the decoder and plots the images – good for a vague idea of what each latent dimension is for.
**plot_single_latent_dim()** - this function, similarlly to plot_all_latent_dim(), creates vectors but focuses on one dimension; It creates series of images (max_value+1) showing progression. E.g if latent_dim = 3 index = 0 and max_value = 3 it would create, pass through the decoder, and later plot following torch tensors [0,0,0], [1,0,0],[2,0,0], and [3,0,0]<br/>
**interactive_latent_image** - this function is the most flexible. It creates a slider for each latent dimension-the range can be changed with min_range, and max_range arguments-and dynamically creates an image based on the current sliders' values.

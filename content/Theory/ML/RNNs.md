Recurrent Neural Networks are designed to process sequential input like text or time series (where the order is important), compared to Feedforward Neural Networks that process input in parallel. The output of a neuron at time step t is fed back as the input to the network at timestep t+1 -- these are called recurrent connections.

Fully Connected RNN
![[Pasted image 20260605194532.png]]
* all outputs feed into all neurons

Unfolded RNN
![[Pasted image 20260605193453.png]]function f θ ![{\displaystyle f_{\theta }}](https://wikimedia.org/api/rest_v1/media/math/render/svg/9874ae06066a2250709085e0fb521eebff2c2fb7) of type ( x t , h t ) ↦ ( y t , h t + 1 ) ![{\displaystyle (x_{t},h_{t})\mapsto (y_{t},h_{t+1})}](https://wikimedia.org/api/rest_v1/media/math/render/svg/daede0f2ff9c38ad773254c9b68cdf2846a65de6) , where

- x t ![{\displaystyle x_{t}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/f279a30bc8eabc788f3fe81c9cfb674e72e858db) : input vector;
- h t ![{\displaystyle h_{t}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/e8dbf3d8bfe322f68ff6400385578f8d78e1ba7c) : hidden vector;
- y t ![{\displaystyle y_{t}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/0fe9554452b93508c9d2479414a45981ecc75a2d) : output vector;
- θ ![{\displaystyle \theta }](https://wikimedia.org/api/rest_v1/media/math/render/svg/6e5ab2664b422d53eb0c7df3b87e1360d75ad9af) : neural network parameters.
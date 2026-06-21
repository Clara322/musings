#past
"learning how to store information over extended time intervals via backprop takes a long time because of the insufficient, decaying backflow" - this is the [[vanishing gradient problem]] in [[RNNs]] 

what's novel: new RNN architecture that has constant error propagation (eg doesn't suffer from vanishing nor exploding gradienet problem) called LSTM

Constant error carousel = CEC is LSTM main's feature and it is built off the premise: if we can't have vanishing nor exploding gradients, what if the gradient is constant -- how would that work?
* have a unit where the weight is 1 and the activation function is the identity function such that activation = w * f' = 1 * 1 = 1
![[Pasted image 20260609122615.png]]

Only having the CEC means that the $w_{ii}$ of the cell would have to do a lot of work to store semantically relevant things
* input weight conflict: we would have to store the input signal and the previous timestamp signal (new information "store" + keep old information "protect" -- conflicting weight bumps)
* output weight conflict: we would have to expose the mem for the output signal and store the current timestamp signal without sharing ("expose this memory," vs "shield output from it.")

That's why we need gates -- learn different things for different purposes
* input gate - decides how much of the input we should take into account
* output gate - decides how much of the state t to read out
* forget gate - decides how much of t-1 state we should take into account
* candidate - the input at time t itself
![[Pasted image 20260609180035.png]]

it contains state at each time step which is different from hidden layers in default deep nets (how?) - because activations in hidden layers disappear after one input/output computation but for RNN state it remains
$h_t = tanh(W_{hh} · h_{t-1} + W_{xh} · x_t + b)$

The LSTM architecture has a series of gates -- this has turned out to be really efficient ant to matter significantly 
* people have researched in depth what happens if you remove/tweak some of the components and the overall performance of the LSTM decreases significantly

**How did they make it so efficient first try??**



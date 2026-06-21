Gradients are generally computed through back propagation - because neural nets are quite deep, there are many multiplications being done with values that are <=1 (because of activation functions like tanh), so the gradient becomes magnitude levels smaller the earlier the layer is (vs later layers)

so it takes more and more time to train connections that are further away (sometimes it becomes impossible because the nudge becomes tiny far enough away)

Consequently, the gradients of earlier weights will be exponentially smaller than the gradients of later weights. This difference in gradient magnitude might introduce instability in the training process, slow it, or halt it entirely

The inverse of that is the exploding gradient problem.
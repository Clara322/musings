#future 

Source: https://blog.jxmo.io/p/there-is-only-one-model

Some people think of learning as a compression problem -- we are compressing all the data in the world. Turns out that models which are better at compression know more about the real world 


*This is pretty cool*:
	Generalization only begins when compression is no longer possible, since the model can’t store data points separately and is forced to combine things.

In this article, [[The Platonic Representation Hypothesis]] is backed up by something called vec2text -- taking a model vector embedding, vec2text can get the original text out. It all argues that models are converging to a shared representation space, and this is becoming more true as we make models bigger and smarter. And it is at minimum true for vision and text models.

vec2text worked through iterative refinement and got to 94% accuracy: sharing vectors, apparently, is equivalent to sharing the text those vectors represent.

Then, what about universality? If we can do vec2text, can we do vec2vec for any representation of vec (because of PRH?) -- the answer is yes! vec2vec was achieved - reveals that all encoders—regardless of architecture or training data—learn nearly the same representations

vec2vec can translate embeddings generated from unseen documents by unseen encoders while preserving their geometry: _i.e.,_ the cosine similarity of the translated embeddings and the _ideal_ target embeddings is high

THE LATENT SPACE STRUCTURE IS THE PROPERTY OF THE TEXT EMBEDDINGS NOT JUST THE DATA

vec2vec https://arxiv.org/abs/2505.12540
>  We introduce the first method for translating text embeddings from one vector space to another without any paired data, encoders, or predefined sets of matches. Our unsupervised approach translates any embedding to and from a universal latent representation (i.e., a universal semantic structure conjectured by the Platonic Representation Hypothesis). Our translations achieve high cosine similarity across model pairs with different architectures, parameter counts, and training datasets.


-------
https://www.youtube.com/watch?v=dO4TPJkeaaU
https://www.lesswrong.com/posts/KqgujtM3vSAfZE2dR/on-ilya-sutskever-s-a-theory-of-unsupervised-learning#Kolmogorov_Complexity__20_48_
https://www.youtube.com/watch?v=l6DKRf-fAAM
https://arxiv.org/abs/2309.10668 (Language Modelling is Compression)


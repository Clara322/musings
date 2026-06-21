#future 

or: the researchers only care about the weights but that is probably a mistake

https://yoonholee.com/blog/2026/we-should-take-text-optimization-more-seriously/

>Text artifacts have a useful inductive bias. The usual Kolmogorov-style compression intuition applies: short specifications that explain many cases are more likely to capture real structure than long lists of exceptions. In this sense, good text updates are _compact patches to a pretrained world prior_. Empirically, text optimization is orders of magnitude more sample-efficient in the low-data regime ([1](https://arxiv.org/abs/2103.08493), [2](https://arxiv.org/abs/2012.15723), [3](https://arxiv.org/abs/2507.19457)). Because of this, a recurring pattern at scale is to use the text layer to elicit and compose existing capabilities in the model, and then distill this into the weights over time ([Anthropic](https://www.anthropic.com/index/claudes-constitution), [OpenAI](https://openai.com/index/deliberative-alignment/), [Cursor](https://cursor.com/cursorbench), [Letta](https://github.com/letta-ai/context-constitution), [Hippocratic AI](https://hippocraticai.com/polaris-3/), [Harvey](https://trajectory.ai/field-notes/the-sovereign-path-for-continual-agent-learning-early-results-on-harvey-lab-with-nvidia-nemotron)).

We should start treating LLMs as systems rather than just look at weights as golden standard -- how can we incorporate prompts, context, memories etc to create a continual learning pipeline that would potentially lead to self improving architectures

Reflective learning https://arxiv.org/abs/2603.28052 is basically an end to end optimisation of the harness where the agent improves the code around the weights (aka the harness itself)

Interesting future questions:
* how to translate memories/context into meaningful learning (weights) even at runtime -- continuous learning?
	>The mechanics of how to evolve the text layer and use it to improve the weights over time is an interesting open research question, whether through direct distillation, ([1](https://arxiv.org/abs/2209.15189), [2](https://arxiv.org/html/2601.19897v1), [3](https://arxiv.org/abs/2602.12275), [4](https://arxiv.org/abs/2603.16856)), synthetic data generation ([5](https://arxiv.org/abs/2504.21798), [6](https://arxiv.org/abs/2601.16443), [7](https://arxiv.org/abs/2602.21193), [8](https://arxiv.org/abs/2604.25727)), modifying the training loop itself ([9](https://arxiv.org/abs/2603.08640), [10](https://arxiv.org/html/2604.14116v1)), or fast-slow learning frameworks ([11](https://arxiv.org/abs/2605.12484)).
* 
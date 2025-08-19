# truth

**Definition:**
Truth is the property of a statement or belief that, when internalized by a predictive system (such as a human mind, neural network, or statistical model), improves the system's ability to make accurate predictions about the world. Rather than being a binary label (true/false) or a static correspondence to external reality, truth is defined by its practical, measurable effect on performance. Truth is a signed scalar, not a binary.

**Characteristics:**
- Interventional: Truth is determined by comparing the predictive performance of a system with and without the statement in question.
- Relational: The truth of a statement depends on the specific learner, task, and metric used to evaluate performance.
- Scalable: The effect of a statement can be measured on a signed interval from –1 (maximal harm) to +1 (maximal help), with 0 indicating no effect.
- Empirical: Truth is not assigned by inspection or logic alone, but by running counterfactual experiments and measuring outcomes.

The truth value of a statement cannot be measured in isolation.

**Contrast:**
- Unlike classical logic, which treats truth as a binary property, this definition recognizes truth as context-dependent and model-specific.
- Unlike fuzzy logic, which assigns partial truth values based on the statement itself, this approach requires empirical testing to determine the effect.

**Challenging the theory**
In the signed-scalar framework, a statement is “true” only to the extent that its incorporation into the model’s knowledge actually improves predictive performance. That improvement is always measured in the actual model being evaluated, not in some hypothetical ideal reasoner. If the gain in predictive accuracy depends on the model figuring out where the statement applies and where it doesn’t, then the truthiness of that statement implicitly depends on the model’s capacity for boundary inference. In other words, the same sentence can be strongly positive-truth for a model with good boundary inference and negative-truth for one that lacks it.

By “boundary” here we mean the implicit limits of a statement’s validity — its domain of applicability in the total space of possible contexts. Boundary inference is the process of recovering these limits from the statement’s content, its training context, or other background knowledge, without the boundaries being explicitly stated. In the Newtonian/quantum case, the statement “Newtonian mechanics describes the world” is only predictive-positive if the model learns the unspoken qualifier “…for macroscopic, slow-moving, weak-gravity systems.” A model that fails to infer this qualifier will overapply the rule to quantum-scale or relativistic situations and degrade its overall predictions. A model that can infer this scope will internalize the statement as a domain-bounded truth rather than a universal claim, and avoid the mispredictions.

However, if a statement is presented together with its domain-specific boundaries, its truthiness score will almost always be higher than the boundary-blind version. That is because the utility of the statement’s generalization through internalization will no longer be contingent on the model’s ability to perform boundary inference — the safe application range is already embedded in the statement’s representation. In this way, explicitly stated scope plays the same role in this framework as separate, domain-specific axiomatic systems do in classical logic: each system is internally valid but incomplete, and no single system attempts to claim universal authority. In both cases, the boundaries keep a locally reliable rule from becoming a globally harmful overgeneralization.


**Related Terms:**
See also: [truthiness as interventional generalization](../Sources/truth.md) for a detailed discussion of the measurement and implications of truth in predictive systems.

Truthiness as Interventional Generalization

For most of human history, “truth” in philosophy and logic has been treated as a light switch: a statement is either true or false, and that’s it.
This binary view works well for classical propositional logic, but it starts to creak when we think about how real-world learners — human or machine — actually use information.

When a predictive system (a human mind, a neural net, even a weather model) believes a statement, the value of that belief is not simply whether the statement matches an external reality.
Instead, the important question is:

“If the system internalizes this statement as fact, will its predictions about the world improve, worsen, or stay the same?”

This shift takes truth from being a binary label to being a performance effect.
We call the measurement of this effect Interventional Generalization.

The Idea

Let’s imagine we have:

A predictive engine — could be a neural network, a statistical model, or a person.

A statement 
s
s — something the engine might believe.

A way to measure performance — for example, how accurate the predictions are on fresh data.

We run two experiments:

Without 
s
s: train or configure the predictive engine in the normal way.

With 
s
s: train/configure it exactly the same way, except we “bake in” 
s
s as a hard rule, a strong prior, or a piece of fixed knowledge.

We then compare how well the two versions perform on the same test data.

If the “with 
s
s” version performs better, 
s
s has positive truthiness.

If it performs worse, 
s
s has negative truthiness.

If there’s no change, 
s
s is predictively inert.

Why This Is Different from Fuzzy Logic

In fuzzy logic, you might assign a statement a number between 0 and 1 to represent partial truth.
Our approach is more cautious: you can’t assign a truthiness score just by looking at the statement itself or at the world.
You can only find it by running the counterfactual experiment — comparing a learner without 
s
s to the same learner with 
s
s.

Truthiness is relational and model-dependent. It depends on this learner, this task, and this way of measuring performance.

Scaling to a Signed Interval

To make truthiness more interpretable, we scale the effect to a number between –1 and 1:

+1 would mean the belief maximally improves predictive performance (though in practice it’s unreachable).

–1 would mean it maximally harms performance (also unreachable in practice).

0 means it makes no measurable difference.

The sign tells us whether the statement helps or harms; the size tells us how strong the effect is.

Measuring in Practice

Pick a performance score — e.g., accuracy, log-likelihood, or some other metric relevant to your predictions.

Train/test without 
s
s, record the score.

Train/test with 
s
s baked in, record the score.

Compare the two scores.

Repeat the process many times to average out randomness.

The truthiness is the average change in performance, rescaled to the (–1, 1) range.

Why This Matters

This reframing makes “truth” not an abstract absolute but a practical, testable quantity.
It acknowledges that a belief’s value depends on how it interacts with a specific mind or machine.
It also forces humility: a belief that helps one learner might harm another.

By defining truthiness in this interventional generalization way, we move from a rigid, binary world to one that reflects how knowledge actually works in predictive systems — messy, context-dependent, and measurable only through careful counterfactual comparison.
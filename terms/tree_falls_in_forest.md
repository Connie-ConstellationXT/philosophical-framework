# if a tree falls in a forest...

**Definition:**
A philosophical riddle exploring the relationship between physical events, perception, and qualia. In this framework, the concept is formalized as an interface and two classes:

```csharp
interface Noise { /* implementation */ }

class AuditoryQualia : Noise
{
    /* implementation */
}

class MaterialOscillator : Noise
{
    /* implementation */
}

/*
 * "If a tree falls in the forest and no one is around to hear it,
 *  does it make a noise?"
 */
void Riddle()
{
    MaterialOscillator treeFall = new MaterialOscillator();
    treeFall.As<AuditoryQualia>(); // doesn’t compile
    Noise noises = new Noise();   // neither does this
}
```

**Notes:**
- The riddle highlights the distinction between physical phenomena (MaterialOscillator) and subjective experience (AuditoryQualia).
- In this formalization, `MaterialOscillator` represents the objective event (tree falling), while `AuditoryQualia` represents the subjective experience of sound.
- The inability to cast or instantiate these types directly reflects the philosophical gap between physical reality and qualia.
- The interface `Noise` is implemented by both, but the mapping between them is not guaranteed or directly accessible.
- This models the epistemic uncertainty at the heart of the riddle: does unperceived sound exist as qualia, or only as physical oscillation?

**Related terms:**
- [Qualia](qualia.md)
- [Epistemology](epistemology.md)
- [Consciousness](consciousness.md)

---
*Add your own notes, references, or reflections below.*

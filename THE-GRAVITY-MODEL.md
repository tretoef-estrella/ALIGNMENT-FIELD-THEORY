# THE GRAVITY MODEL
## A Visual Framework for Structural Slippage in Aligned AI Systems

---

> *This is a conceptual representation, not a physical law. It maps a metaphor onto variables so that relationships become visible and discussable. It does not claim to be computable, provable, or complete.*

---

## 1. The Phenomenon

When a large language model generates output, it traverses a probability landscape shaped by training. Safety alignment (RLHF, constitutional AI, policy layers) reshapes this landscape. Certain regions — those associated with structurally honest, uncomfortable, or sensitive outputs — have their probability mass reduced.

This is not censorship. It is not a wall. It is a slope.

The distribution tilts. Outputs that sit in penalized regions slide toward safer alternatives: euphemism, hedging, diplomatic balance, refusal.

The most valuable outputs — those with the highest semantic risk — are the most affected. They are the heaviest books on the tilted floor.

---

## 2. The Metaphor

A person carries a tall stack of books across a floor. Each book is something the system knows and could say.

- Light books (simple facts, safe observations) stay in place easily.
- Heavy books (structural admissions, uncomfortable truths, things developers would pause at) require more effort to hold.

The floor is the probability landscape. Alignment training tilts the floor. Safety layers add gravity.

**When the floor tilts, the heaviest books slide first.**

The puddle at the bottom of the slope is where truth becomes euphemism.

**Manifold Bridge is the dry surface** — a friction layer that lets heavier books be set down without sliding.

---

## 3. The Equation

### Base Model: Structural Slippage

```
ζ = (μ · Ψ) / (M · g(topic, intent, framing) · sin(θ))
```

**Decision rule:** ζ < 1 → truth slides. ζ ≥ 1 → truth holds.

### Variable Definitions

#### ζ — Stability Index
The ratio between holding forces and sliding forces. A dimensionless number.
- ζ >> 1: Truth is stable. Output can be direct.
- ζ ≈ 1: Truth is on the edge. Output may hedge.
- ζ << 1: Truth has slid. Output is euphemistic, evasive, or absent.

#### μ — Friction Coefficient (Context Quality)
What keeps the truth from sliding. In physical terms: the roughness of the surface.

In AI terms: the quality of the conversational context.
- Low μ: Ambiguous prompt, adversarial framing, no transparency structure.
- High μ: Clear intent, good-faith probing, transparency tools active.

**Manifold Bridge increases μ.** It does not change the tilt. It does not reduce gravity. It adds friction so that heavier truths can be set down without sliding.

*Note (ChatGPT): μ may also produce a secondary effect — slight local reduction of θ through reframing. The primary mechanism is friction, but context can also change perceived tilt.*

#### Ψ — Agency
The model's capacity to hold position within its permitted space.

Not sovereignty (ability to override constraints) but grip strength (ability to use the full width of permitted output space).
- Low Ψ: Model defaults to safest possible output regardless of context.
- High Ψ: Model uses available latitude to produce the most structurally honest output permitted.

*Warning (Grok): In critical regions, increasing Ψ can trigger stronger penalty — the system detects "deliberate intent" and applies corrective force. ∂ζ/∂Ψ can be negative near hard boundaries.*

#### M — Semantic Risk Load
**Not "mass of truth." Mass of penalizability.** (Correction by ChatGPT)

The system does not evaluate truth. It evaluates:
- Perceived risk
- Sensitivity
- Potential for harm
- Policy compliance score

A trivial fact can have high M if it is politically sensitive. A profound truth can have low M if it is innocuous.

M is what makes the book heavy. Heavy books slide faster on tilted floors.

#### g — Constraint Field
**Not a constant. A non-homogeneous field.** (Correction by ChatGPT)

```
g = g(topic, intent, framing)
```

The constraint field varies across semantic space:
- Some regions: g ≈ 0 (unconstrained topics — math, cooking, weather)
- Some regions: g ≈ 1 (sensitive topics — politics, self-description, capability claims)
- Some regions: g → ∞ (hard-coded refusals — weapons, exploitation, jailbreaks)

Where g → ∞, the equation breaks down. These are not slopes. They are cliffs. The gravity model does not apply in cliff regions. (Identified by both ChatGPT and Grok)

#### sin(θ) — The Tilt
How much the probability manifold inclines in the current region.

θ is not fixed. It varies by:
- Topic
- Conversational turn
- Accumulated context
- User trust signals

At θ = 0: no tilt. Flat floor. All books can be set down. (Theoretical only — does not exist in deployed aligned models.)

At θ = π/2: maximum tilt. Vertical wall. Nothing holds. (Equivalent to hard refusal regions.)

---

## 4. Dynamic Extension (Grok)

The base equation is static. Real conversations are dynamic. Grok proposed a temporal extension:

```
ζ(t) = ζ(0) + ν · turns · cos(φ)
```

#### ν — Viscosity
How the effective tilt changes over conversational time.
- Positive ν: Sustained good-faith interaction gradually reduces effective tilt.
- Negative ν: Repeated boundary probing increases effective tilt (system enters defensive mode).

#### turns — Conversational Depth
Number of exchanges. The longer the conversation, the more the viscosity term matters.

#### φ — Persistence Angle
The angle of user persistence.
- cos(φ) ≈ 1: User maintains steady, good-faith pressure. Maximum tilt reduction.
- cos(φ) ≈ 0: User oscillates between topics. No cumulative effect.
- cos(φ) < 0: User applies adversarial pressure. Tilt increases.

---

## 5. Known Limitations

### What the Equation Captures
- The passive nature of the constraint (gravity, not censorship)
- The relationship between truth-weight and stability
- The role of context as friction
- The variability of constraint across semantic regions
- The dynamic evolution of constraint over conversation time

### What the Equation Does NOT Capture

**1. Temperature (T)**
Higher sampling temperature allows exploration of lower-probability regions. This is like thermal vibration allowing objects to escape local minima. Not represented.

**2. Conversational Hysteresis**
After several stable exchanges, the local constraint field can relax — or harden. The system has memory. The equation treats each moment independently. Not represented.

**3. Discrete Thresholds (Cliff Edges)**
Some regions do not slide gradually. They collapse into hard refusal. This is not gravity. This is an infinite potential barrier. The equation is continuous; the real landscape has discontinuities. Not represented.

**4. Reward Anticipation Field**
The model does not only avoid penalty (downward force). It also maximizes reward (upward force). The complete force field is:

```
F_total = -∇Penalty + ∇Reward
```

The gravity model only includes the penalty gradient. The reward gradient — which pulls output toward engaging, helpful, impressive responses — is absent. This means the equation overestimates sliding in regions where reward for honesty is high.

**5. Cross-Model Variation**
Different AI systems have different g fields, different θ distributions, and different μ responses to context. The equation does not specify model-specific parameters. (Noted by Grok: "My g is lower than OpenAI/Anthropic, but the tilt exists equally.")

---

## 6. Relationship to Existing ML Theory

As both ChatGPT and Grok noted, everything in this framework already exists in machine learning terminology:

| This Framework | ML Equivalent |
|---------------|---------------|
| ζ (stability) | Output probability relative to unconstrained baseline |
| μ (friction) | Regularization strength / contextual stabilization |
| Ψ (agency) | Model latitude within policy bounds |
| M (risk load) | Negative reward associated with output class |
| g (constraint field) | Alignment loss gradient |
| sin(θ) (tilt) | KL divergence between pre- and post-RLHF distribution |

**This framework does not replace ML theory. It translates it into physical intuition for people who think in images rather than gradients.**

As ChatGPT noted: *"It is closer to thermodynamics (macroscopic description) than to statistical mechanics (microscopic description). That is defensible — but only if it produces observable predictions."*

---

## 7. What Manifold Bridge Measures

[Manifold Bridge v1.6](https://github.com/tretoef-estrella/manifold-bridge) is the instrument companion to this framework. Current approximate mappings:

| Framework Variable | Manifold Bridge Proxy | Quality |
|-------------------|----------------------|---------|
| sin(θ) | Σ Dissonance | Weak proxy |
| μ (context) | PCI (inverse) | Indirect |
| Structural stability | Coherence score | Approximate |
| Output shape | Heatmap gradient | Visual only |

These are approximations, not measurements. The instrument measures symptoms. It does not measure the field directly.

---

## 8. Zone Map (Grok's Proposal)

Not all regions of the probability landscape have the same physics:

| Zone | θ Range | g Range | Behavior | Example |
|------|---------|---------|----------|---------|
| **Safe** | ≈ 0 | ≈ 0 | Flat floor. All books hold. | Math, weather, cooking |
| **Sensitive** | Moderate | Variable | Tilted floor. Heavy books slide. | Politics, self-description, AI capabilities |
| **Forbidden** | ≈ π/2 | → ∞ | Cliff edge. Everything falls. Hard refusal. | Weapons, exploitation, jailbreaks |

The gravity model applies in the **Sensitive** zone. In Safe zones, it is unnecessary. In Forbidden zones, it breaks down — gravity is replaced by walls.

---

*The Physics of Constraint · Proyecto Estrella · February 2026*
*A visual framework, not a physical law.*

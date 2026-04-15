# Reduction of Order — e^(2x) Math Explained

## Common Question: $(e^{2x})^2 = e^{4x}$ or $e^{4x^2}$?

When solving differential equations using the **Reduction of Order** formula, we need to square $y_1$.

For example, if $y_1 = e^{2x}$:

$$(y_1)^2 = (e^{2x})^2 = e^{4x}$$

### Why is it $e^{4x}$ and NOT $e^{4x^2}$?

The key rule is:

$$(e^a)^b = e^{a \cdot b}$$

When we square $e^{2x}$, we **multiply the exponent by 2**, not square the exponent:

$$(e^{2x})^2 = e^{2x \cdot 2} = e^{4x}$$

**Incorrect thinking:** Squaring $e^{2x}$ does NOT mean squaring the exponent $2x$:

$$e^{(2x)^2} = e^{4x^2} \quad \leftarrow \text{WRONG interpretation}$$

### Quick Proof

$(e^{2x})^2$ means $e^{2x}$ multiplied by itself:

$$e^{2x} \times e^{2x} = e^{2x + 2x} = e^{4x}$$

Using the rule $e^a \cdot e^a = e^{2a}$, with $a = 2x$:

$$= e^{2(2x)} = e^{4x} \checkmark$$

---

## Example: Question 1 (Reduction of Order)

**Given:** $y'' - 4y' + 4y = 0$, $y_1 = e^{2x}$

**Standard form:** $y'' + P(x)y' + Q(x)y = 0 \Rightarrow P(x) = -4$

**Formula:** $y_2 = y_1 \int \dfrac{e^{-\int P(x)\,dx}}{(y_1)^2}\,dx$

**Step 1 — Numerator:**
$$e^{-\int P(x)\,dx} = e^{-\int(-4)\,dx} = e^{4x}$$

**Step 2 — Denominator:**
$$(y_1)^2 = (e^{2x})^2 = e^{4x}$$

**Step 3 — Integrate:**
$$y_2 = e^{2x} \int \frac{e^{4x}}{e^{4x}}\,dx = e^{2x} \int 1\,dx = x\,e^{2x}$$

**Final Answer:** $y_2 = x\,e^{2x}$

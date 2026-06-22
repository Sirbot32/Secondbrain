# Learning Queue

Persistent list of things I've identified I don't know or am unsure about. Check items off (change `[ ]` to `[x]`) once learned — don't delete them, so there's a record.

## AI
- [ ] How multiple inputs combine at a single neuron (weighted sum + bias) before the activation function
- [ ] What activation functions (sigmoid, tanh, ReLU) are and why they're needed (introducing non-linearity)
- [ ] The precise/structural reason hidden layers are called "hidden" (position between input and output, not about who configures it)
- [ ] How backpropagation/gradient descent actually works to update weights (the standard training method for most deep learning, vs. genetic algorithms)
- [ ] What deep learning specifically is, and the correct hierarchy between AI, machine learning, and deep learning (currently have it backwards)
- [ ] What training data for large language models (e.g. ChatGPT) actually consists of, and what a "token" is
- [ ] The actual technical mechanism behind AI hallucination (beyond "lacks instinct") — i.e. statistical generation without built-in truth-verification
- [ ] Which specific math functions are actually used in neural nets (e.g. tanh = hyperbolic tangent, not trig tangent; sigmoid relates to log) vs. which (plain sine/cosine) aren't generally relevant outside niche cases like transformer positional encoding

## Philosophy
- [ ] Boethius's classical solution to the foreknowledge problem — God perceiving all of time at once (not sequential foreknowledge) — as a distinct answer from the fourth-dimension/eternalism framing
- [ ] Block universe / eternalism as a named view in philosophy of time
- [ ] Compatibilism (the standard version — redefining "free" as "uncoerced," with no dimensional/eternalism framework needed at all)
- [ ] The aggregation problem / separateness-of-persons critique of utilitarianism — the named version of the torture-case objection already worked out independently
- [ ] Doctrine of double effect (harm as side-effect vs. harm as direct means) as the formal explanation for the trolley switch/push intuition split
- [ ] Kant's means/ends formula ("never use a person merely as a means to an end") as it applies to the trolley push case
- [ ] Theodicy / problem of evil — the standard arguments for why an all-powerful, good being would allow suffering, and how they relate to (or could rebut) the foreknowledge/fairness argument — flagged as adjacent but not yet explored

## Math
- [ ] What a derivative actually measures (the concept of rate of change, before the formula)
- [ ] Why prime numbers matter for encryption specifically, beyond the basic "only divisible by 1 and itself" definition
- [ ] What a limit is, in the calculus sense (the concept that precedes derivatives)
- [ ] The precise definition of a function (exactly one output per input) and how to test whether a given equation satisfies it — initially conflated "function" with "linear equation" / "outputs only real numbers," and misapplied the correct rule when tested against a circle equation (x² + y² = 1)

## Logic
- [x] The precise definition of the NOT operator (single input, inverts true to false and false to true) — answer was unclear/incomplete
- [ ] How binary place-value actually works (powers of 2) — e.g. decimal 2 = binary "10", decimal 3 = binary "11" — attempts to write these out were incorrect (retried: decimal 5 given as "111", which is actually 7)
- [ ] Why two-state (binary) circuits are preferred in hardware over multi-state ones — the deeper engineering reason (narrower voltage bands between states = easier for noise to cause misreads), beyond "it plugs into logic gates" or "current takes the path of least resistance"
- [x] What a logic gate physically/mechanically does inside a chip (e.g. how transistors implement AND/OR/NOT via voltage) — correctly extended this to wiring an OR gate's transistors in parallel
- [ ] The difference between an argument's validity and the truth of its conclusion (formal logic) — currently conflates "invalid" with "always false"; needs the validity/truth independence to click (valid arguments can have false conclusions, invalid arguments can have true ones)
- [ ] The formal name for the fallacy just correctly diagnosed by reasoning alone: "affirming the consequent" — applied to a new example ("divisible by 4 → even, 6 is even, therefore 6 is divisible by 4") but misnamed it "false equivalence"
- [ ] How ternary (base-3) computing actually worked in practice (e.g. the Setun computer) and the real engineering reason it's impractical at scale vs. binary

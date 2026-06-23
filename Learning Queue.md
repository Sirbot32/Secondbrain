# Learning Queue

Persistent list of things I've identified I don't know or am unsure about. Check items off (change `[ ]` to `[x]`) once learned — don't delete them, so there's a record.

## Stocks
- [ ] How order-flow imbalance actually moves price in the order book — currently has the direction backwards: thinks a large sell order pushes price *up* and a large buy order pushes price *down*. Actually: a large sell order eats through the bid stack top-down (price falls), a large buy order eats through the ask stack bottom-up (price rises). Resource: [Orders and the order book — Optiver](https://www.optiver.com/explainers/orders-and-the-order-book/)
- [ ] What market cap is and how it's calculated — not yet asked. Resource: [Market Cap Explained — FINRA](https://www.finra.org/investors/insights/market-cap)
- [ ] What a P/E ratio is trying to tell you — not yet asked. Resource: [What Is the P/E Ratio? — Charles Schwab](https://www.schwab.com/learn/story/stock-analysis-using-pe-ratio)
- [ ] What short selling is and why its risk profile differs from a normal long trade — not yet asked. Resource: [Short Selling: The Risks and Rewards — Charles Schwab](https://www.schwab.com/learn/story/ins-and-outs-short-selling)
- [ ] The difference between a stock split and an actual change in company value — not yet asked. Resource: [Stock Splits — FINRA](https://www.finra.org/investors/investing/investment-products/stocks/stock-splits)

## AI
- [ ] How multiple inputs combine at a single neuron (weighted sum + bias) before the activation function
- [ ] What activation functions (sigmoid, tanh, ReLU) are and why they're needed (introducing non-linearity)
- [ ] The precise/structural reason hidden layers are called "hidden" (position between input and output, not about who configures it)
- [ ] How backpropagation/gradient descent actually works to update weights (the standard training method for most deep learning, vs. genetic algorithms)
- [ ] What deep learning specifically is, and the correct hierarchy between AI, machine learning, and deep learning (currently have it backwards)
- [ ] What training data for large language models (e.g. ChatGPT) actually consists of, and what a "token" is
- [ ] The actual technical mechanism behind AI hallucination (beyond "lacks instinct") — i.e. statistical generation without built-in truth-verification
- [ ] Which specific math functions are actually used in neural nets (e.g. tanh = hyperbolic tangent, not trig tangent; sigmoid relates to log) vs. which (plain sine/cosine) aren't generally relevant outside niche cases like transformer positional encoding
- [ ] What overfitting is in a machine learning model — no attempt made
- [ ] What a "loss function" is in machine learning — no attempt made
- [ ] What the Turing Test is — no attempt made
- [ ] The difference between supervised, unsupervised, and reinforcement learning — no attempt made
- [ ] The difference between a parameter and a hyperparameter — no attempt made
- [ ] What gradient descent is minimizing and how it picks a direction to move — no attempt made
- [ ] What a transformer's "attention" mechanism does — no attempt made
- [ ] Why LLMs need vastly more training data than humans need for language — answer leaned on a plausible-sounding intuition (humans not "noticing" they're learning) rather than the actual reasons (humans get multimodal/embodied grounding, innate language-learning priors, and efficient few-shot generalization that current model architectures lack)
- [ ] The difference between a compiler and an interpreter — no attempt made
- [ ] What Big O notation measures and why it matters for algorithm choice — no attempt made
- [ ] The difference between a stack and a queue, with real-world examples — no attempt made
- [ ] What encryption is doing mathematically (public/private key, beyond "primes matter") — no attempt made

## Philosophy
- [ ] Boethius's classical solution to the foreknowledge problem — God perceiving all of time at once (not sequential foreknowledge) — as a distinct answer from the fourth-dimension/eternalism framing
- [ ] Block universe / eternalism as a named view in philosophy of time
- [ ] Compatibilism (the standard version — redefining "free" as "uncoerced," with no dimensional/eternalism framework needed at all)
- [ ] The aggregation problem / separateness-of-persons critique of utilitarianism — the named version of the torture-case objection already worked out independently
- [ ] Doctrine of double effect (harm as side-effect vs. harm as direct means) as the formal explanation for the trolley switch/push intuition split
- [ ] Kant's means/ends formula ("never use a person merely as a means to an end") as it applies to the trolley push case
- [ ] Theodicy / problem of evil — the standard arguments for why an all-powerful, good being would allow suffering, and how they relate to (or could rebut) the foreknowledge/fairness argument — flagged as adjacent but not yet explored
- [ ] Moral relativism vs. moral objectivism — no attempt made
- [ ] "The map is not the territory" — what the saying means and a real example of it going wrong — no attempt made
- [ ] The Ship of Theseus paradox and what it illustrates about identity — no attempt made
- [ ] The difference between an argument being valid and being sound (distinct from the validity-vs-truth-of-conclusion gap already logged under Logic) — no attempt made

## Math
- [ ] What a derivative actually measures (the concept of rate of change, before the formula)
- [ ] Why prime numbers matter for encryption specifically, beyond the basic "only divisible by 1 and itself" definition
- [ ] What a limit is, in the calculus sense (the concept that precedes derivatives)
- [ ] The precise definition of a function (exactly one output per input) and how to test whether a given equation satisfies it — initially conflated "function" with "linear equation" / "outputs only real numbers," and misapplied the correct rule when tested against a circle equation (x² + y² = 1)
- [ ] How a derivative and an integral relate to each other (rate of change vs. accumulated area, inverse operations) — no attempt made
- [ ] The geometric meaning of the Pythagorean theorem (areas of squares on each leg summing to the area of the square on the hypotenuse), beyond just the formula — knew the formula but not the geometric picture
- [ ] What Bayes' theorem updates and why it matters for reasoning under uncertainty — no attempt made
- [ ] The difference between necessary and sufficient conditions — no attempt made
- [ ] What "statistically significant" actually means (and doesn't mean) — no attempt made

## Logic
- [x] The precise definition of the NOT operator (single input, inverts true to false and false to true) — answer was unclear/incomplete
- [ ] How binary place-value actually works (powers of 2) — e.g. decimal 2 = binary "10", decimal 3 = binary "11" — attempts to write these out were incorrect (retried: decimal 5 given as "111", which is actually 7)
- [x] Why two-state (binary) circuits are preferred in hardware over multi-state ones — the deeper engineering reason (narrower voltage bands between states = easier for noise to cause misreads) — correctly extended this to a 4-state vs. 3-state case unprompted
- [x] What a logic gate physically/mechanically does inside a chip (e.g. how transistors implement AND/OR/NOT via voltage) — correctly extended this to wiring an OR gate's transistors in parallel
- [ ] The difference between an argument's validity and the truth of its conclusion (formal logic) — currently conflates "invalid" with "always false"; also tried to give an invalid-but-true-conclusion example but gave two unrelated statements with no actual inference between them, not an argument at all
- [ ] The formal name for the fallacy just correctly diagnosed by reasoning alone: "affirming the consequent" — applied to a new example ("divisible by 4 → even, 6 is even, therefore 6 is divisible by 4") but misnamed it "false equivalence"; re-asked, not yet re-attempted
- [ ] How ternary (base-3) computing actually worked in practice (e.g. the Setun computer's "trits" valued -1/0/+1, balanced ternary) — correctly explained *why* binary won out (noise margins), but the "how it actually worked" half is still unaddressed
- [ ] What a syllogism is — no attempt made
- [ ] The difference between deductive and inductive reasoning — defined deductive reasoning as "taking what information you have and creating a conclusion," which is generic enough to also describe inductive reasoning; missing the actual distinguishing feature (deductive: true premises *guarantee* a true conclusion; inductive: premises only make the conclusion probable). Inductive reasoning — no attempt made at all

## History
- [ ] Why and roughly when the Western Roman Empire fell — no attempt made
- [ ] What the Magna Carta is and why it matters — no attempt made
- [ ] The exact timeframe of the Renaissance (started 14th century, not 17th) — origin country (Italy) was correct, century was not, even after a retry
- [ ] The Declaration of Independence (1776) vs. George Washington's first presidential inauguration (1789) — currently conflated into a single 1776 date
- [ ] The specific immediate trigger of WWII (Germany's invasion of Poland, September 1939) as distinct from its underlying causes (Great Depression, Hitler's rise) — causes were correctly identified but not the actual triggering event; also called the 1938 Anschluss a "reunification" of Austria and Germany rather than an annexation
- [ ] Who Hammurabi was and what the Code of Hammurabi actually established — no attempt made
- [ ] Why the Berlin Wall specifically came down in 1989 (Gorbachev-era reforms loosening Soviet control, mass Eastern Bloc protests, a confused East German announcement crowds acted on immediately) — correctly knew civilians tore it down, but not the actual causal chain
- [ ] When the Industrial Revolution started (mid-to-late 18th century, i.e. the 1700s — not the 17th century/1600s) and one concrete way it changed labor (e.g. shift from agrarian/craft work to factory wage labor) — hedged between two centuries and gave only a vague "changed how we viewed labor" answer
- [ ] What the Treaty of Versailles actually did (imposed harsh reparations and a "war guilt" clause on Germany, redrew European borders, created the League of Nations) — self-corrected to the right basic facts (the WWI-ending treaty, signed at Versailles, not WWII or Paris), but the actual terms/consequences are still a gap
- [ ] The precise federal structure of the legislative/executive/judicial branches — currently describes the legislative branch as state-level officials handling in-state matters, when it's actually Congress (House + Senate) operating at the federal level; states have their own separate legislatures. The veto-override mechanism (2/3 vote in both chambers, not just one) also needs tightening.
- [ ] The precise definition of capitalism as an economic system, beyond "a system of growth" — no confident answer given

## Earth Science
- [ ] What causes earthquakes — currently thinks it's "mantle rotation" (not a real geological mechanism); actually caused by tectonic plates grinding against each other at fault lines, building up stress that releases suddenly as seismic waves

## Astronomy
- [ ] What causes the phases of the moon — thinks it's "the moon casting a shadow when it enters our atmosphere" (the moon never enters Earth's atmosphere; this conflates phases with the separate, much rarer lunar-eclipse mechanism); correctly had that the sun only lights the half of the moon facing it, but missed that this half is *always* lit — phases come from the changing Earth-Moon-Sun angle as the moon orbits, which changes how much of that lit half is visible from Earth, not from the lit portion itself changing

## Chemistry
- [ ] The difference between an isotope and an ion — currently conflated: described isotopes as differing in electron count (which actually describes an ion/charge), when isotopes actually differ in neutron count while having the same number of protons and electrons
- [ ] What entropy means, in plain terms — no attempt made

## Economics
- [ ] The difference between inflation and deflation, and why mild inflation is generally considered healthy — no attempt made
- [ ] What it means for a central bank to "raise interest rates" and why it would do that — no attempt made
- [ ] The difference between GDP and GNP — no attempt made
- [ ] How inflation is actually measured/calculated — no attempt made
- [ ] The difference between a tax deduction and a tax credit — no attempt made

## Language
- [ ] The difference between "affect" and "effect" — no attempt made
- [ ] What a metaphor is (as distinct from a simile) — simile was correctly defined, metaphor was not recalled
- [ ] The difference between active and passive voice, and when passive voice is actually useful — no attempt made

## Psychology
- [ ] Operant conditioning, and how it differs from classical conditioning (classical conditioning itself already confirmed) — no attempt made
- [ ] What cognitive dissonance is — no attempt made
- [ ] What confirmation bias is — no attempt made
- [ ] The difference between intrinsic and extrinsic motivation — no attempt made
- [ ] The Dunning-Kruger effect — no attempt made

## Geography
- [ ] What causes the seasons — opened with the "closer to the sun = warmer" distance misconception, then described axial tilt as one hemisphere "facing the sun closer" rather than receiving more direct/concentrated sunlight and more daylight hours; did correctly have that the hemispheres are out of phase (northern winter = southern summer). Actual cause: Earth's ~23.5° axial tilt changes the angle sunlight hits each hemisphere and day length, not physical distance to the sun (Earth is actually closest to the sun during Northern Hemisphere winter)

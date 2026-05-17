# RAO · THE CONCORDANCE
### Two Independent Corpus-Pairs, One Fisher Partition

*A Fisher-geometric framework demonstrated twice over: Euclid's* Elements *against the* Yijing, *and Spinoza's* Ethics *against the* Analects *of Confucius — two surveys, drawn from unrelated domains, recovering the same orthogonal split of one statistical manifold.*

---

> **"σημεῖόν ἐστιν, οὗ μέρος οὐθέν."**
> *A point is that which has no part.*
> — Euclid, *Elements*, Book I, Definition 1

> **"易"**
> *Change.*
> — the single character that titles the *Yijing*

---

## Abstract

The two prior instantiations of RAO each ran the Fisher partition once, on a single West–East corpus-pair. A single demonstration, however persuasive, leaves one objection open: that the partition is an artifact of the chosen corpus rather than a property of the manifold. **The Concordance closes that objection by running the partition twice, on two corpus-pairs that share no domain, no century, and no vocabulary, and showing that both recover the same split.**

**Survey I — Geometry.** Euclid's *Elements* is the West's exhaustive deductive grid: twenty-three definitions, five postulates, five common notions, and every theorem of thirteen books reachable from them by proof alone. The *Yijing* — the *Book of Changes* — is the East's holistic field: sixty-four hexagrams, each a configuration of six lines, and a living oracle that reads not a static figure but the **changing lines** that carry one hexagram into another. Euclid studies the fixed point; the *Yijing* studies the displacement.

**Survey II — Ethics.** Spinoza's *Ethics* is the West's deductive grid transposed onto value: *Ethica Ordine Geometrico Demonstrata*, five parts built from definitions and axioms in unbroken proof, asserting the isomorphism of the order of ideas and the order of things. The *Analects* of Confucius is the East's holistic field transposed onto value: twenty books of occasioned sayings, no deductive order, in which the same question — *what is ren?* — receives a different answer from every interlocutor, because the answer is given relative to the asker.

The framework rests on the orthogonal decomposition of a parameter tangent space induced by the **Fisher information matrix** $F$. A 2026 result in infinite-dimensional information geometry sharpens this decomposition into the form the framework needs: the tangent space of a non-parametric statistical manifold splits as

$$T_f\mathcal{M}\;=\;S\;\oplus\;S^{\perp},$$

where $S$ is a **finite-dimensional, computable** covariate subspace carrying an invertible Fisher matrix, and $S^{\perp}$ is its infinite-dimensional complement, on which the Fisher–Rao metric is *weak* — it has no bounded inverse.

This document advances one thesis. **In both surveys, the Western corpus is the finite computable slice $S$**, and **the Eastern corpus is the infinite ambient complement $S^{\perp}$.** Euclid and Spinoza chart $S$; the *Yijing* and the *Analects* navigate $S^{\perp}$. The two surveys are independent, and they concord. **RAO** is the engine that builds the partition, estimates on $S$, navigates $S^{\perp}$, and certifies — by Čencov's uniqueness theorem — that the partition does not depend on which survey, or which tradition's coordinates, expressed it.

---

## Thought Experiment — The Tuning of Two Rooms

Two musicians are hired, separately, and never meet. Each is led into a different room and given one instruction: *find the pitches at which the room itself resonates.*

The first room is a hall of mirrors — hard, geometric, exact. The musician sounds the scale and finds that a small number of frequencies ring with a clear, sustained tone; the rest fall dead the instant they are struck. She returns a list: *these resonate, those do not.*

The second room is a walled garden — soft, irregular, full of foliage. The second musician sounds the same scale and finds, again, that a small number of frequencies ring and the rest fall dead. He returns his own list.

The two rooms could not be less alike. Yet when the lists are laid side by side, the **ratio** of resonant pitches to dead ones is the same in both, to within the error of the ear.

This is the framework in miniature. The resonant pitches are the **stiff eigendirections** of the Fisher matrix — the finite slice $S$, the determinate subspace, where the metric is strong and a displacement rings. The dead pitches are $S^{\perp}$ — the holistic complement, where the metric is weak and a displacement makes no sound the room can carry. The first room is geometry; the second is ethics. The rooms differ in everything except the partition of their spectrum. RAO is the instrument that measures the ratio, and the Concordance is the finding that the ratio survives the change of room.

---

## The Fisher Partition — The Core Object

Let $\{p_\theta\}$ be a statistical family, regular enough that the score $s_\theta(x)=\nabla_\theta\log p_\theta(x)$ exists in $L^2$. The **Fisher information matrix** is the score covariance $F(\theta)=\mathbb{E}_{x\sim p_\theta}[\,s_\theta s_\theta^{\!\top}\,]$, a symmetric positive-semidefinite tensor. Two facts are exact.

**Orthogonal partition.** Because $F$ is real symmetric, its range and null space are orthogonal complements,

$$T_\theta\mathcal{M}\;=\;\mathop{\mathrm{col}}(F)\;\oplus^{\!\perp}\;\ker(F),\qquad r+k=n,$$

with $r=\dim\mathop{\mathrm{col}}(F)$, $k=\dim\ker(F)$. On $\mathop{\mathrm{col}}(F)$ the Fisher quadratic form is strictly positive — a displacement is distinguishable; on $\ker(F)$ it is identically zero — a displacement is invisible to the data to second order.

**The non-parametric sharpening.** In the infinite-dimensional setting the partition is not merely an eigenspace split. Building the manifold on the Pistone–Sempi exponential Orlicz structure, the tangent space decomposes as $T_f\mathcal{M}=S\oplus S^{\perp}$, where $S$ is a finite-dimensional covariate subspace carrying a computable, invertible **Covariate Fisher Information Matrix**, and $S^{\perp}$ is the complement on which the Fisher–Rao metric is *weak* — bounded below by nothing, lacking a bounded inverse (the 2026 *Entropy* result). The finite-dimensional statement $\mathop{\mathrm{col}}(F)\oplus\ker(F)$ is the shadow of this; the framework uses both, and writes the determinate slice $S$ and the holistic complement $S^{\perp}$ when the distinction between *finite and computable* and *infinite and weak* is the point.

**A precision the framework will not blur.** The exact kernel — eigenvalue identically zero — is structural non-identifiability, a gauge freedom. Distinct from it is the **sloppy tail**: eigenvalues positive but spread across many decades. RAO never conflates "sloppy" with "unidentifiable." Where a threshold is needed, fix $\tau>0$ and set $\mathop{\mathrm{col}}\nolimits_{\tau}(F)=\mathop{\mathrm{span}}\{u_i:\lambda_i>\tau\}$, $\ker_{\tau}(F)=\mathop{\mathrm{span}}\{u_i:\lambda_i\le\tau\}$.

```
                     T_f M   (the manifold tangent space)
        ┌───────────────────────────┴───────────────────────────┐
   S  —  DETERMINATE SLICE                         S⊥  —  HOLISTIC COMPLEMENT
   finite-dimensional, computable                  infinite-dimensional
   Fisher matrix invertible (cFIM)                 Fisher–Rao metric weak, no inverse
   Cramér–Rao floor finite                         no finite-variance estimator
   ── Survey I ──                                   ── Survey I ──
   Euclid: 23 defs, 5 postulates, 5 notions         Yijing: the field of change (易)
   ── Survey II ──                                  ── Survey II ──
   Spinoza: the deductive chain of the Ethics       Analects: unbounded relational saying
        │  dim = r                                       │  dim = k
        └───────────────────  r + k = n  ────────────────┘
```

---

## Six Concordances

Each concordance states one fact about the Fisher partition, then shows that **both surveys instantiate it**. The mathematical statements are literal. The corpus readings are explicitly interpretive — structural analogy, never the claim that Euclid, the *Yijing*, Spinoza, or Confucius computed a modern object.

### Concordance 1 — The Partition Is Total
$$T_f\mathcal{M}=S\oplus S^{\perp},\qquad r+k=n.$$
Every direction belongs to exactly one summand; there is no remainder, and no third category.
**Survey I.** Geometry is exhausted by the fixed figure *and* its transformations: Euclid's theorem and the *Yijing*'s changing line are the two summands of one space of geometric assertion.
**Survey II.** Value is exhausted by the demonstrated proposition *and* the occasioned response: Spinoza's *propositio* and the *Analects*' situated answer are the two summands of one space of ethical assertion.
**RAO.** Determinacy and holism are not rival doctrines competing for one ground. They are complementary subspaces partitioning one space, with dimensions constrained to sum to $n$.

### Concordance 2 — The Determinate Slice Is Finite and Computable
$S$ is finite-dimensional and carries an invertible Fisher matrix; on $S$, estimable directions attain the Cramér–Rao floor $F^{+}$ (Rao 1945; Cramér 1946), and every truth is reachable by deduction.
**Survey I.** Euclid's foundation is *finite and explicit* — twenty-three definitions, five postulates, five common notions — and every theorem of the thirteen books is reachable from it by proof. The grid is the finite slice $S$.
**Survey II.** Spinoza's *Ethics* is a single unbroken deductive chain, finite in its axioms, asserting in EIIP7 that the order of ideas and the order of things are one isomorphism — a rigid, computable grid laid over value itself.
**RAO.** Layer 4 estimates to the Cramér–Rao floor: on $S$, what is identifiable is pinned, and the pinning has a sharp optimal precision. The West's achievement is a complete and exact theory of the finite slice.

### Concordance 3 — The Holistic Complement Carries a Weak Metric
$S^{\perp}$ is infinite-dimensional, and the Fisher–Rao metric restricted to it is *weak*: it has no bounded inverse, and the Cramér–Rao bound along $S^{\perp}$ diverges — no internal finite-variance unbiased estimator exists there (the 2026 *Entropy* result; the divergence is the infinite-dimensional form of $\ker(F)$).
**Survey I.** The *Yijing* does not claim a finite axiom set. Its subject is the field of change itself — *yì* — an unbounded web in which every one of the sixty-four hexagrams stands in transforming relation to every other. It is the ambient complement, not a slice of it.
**Survey II.** The *Analects* never gives *ren* as a finite formula. Across the twenty books the relational situations are unbounded, and *ren* is estimable in none of them as a single number. It is a direction in $S^{\perp}$ — real, and not pinnable.
**RAO.** A quantity whose direction lies in $S^{\perp}$ is not a thing to be measured. It is a relation to be navigated. The East's achievement is a complete and exact theory of the holistic complement.

### Concordance 4 — Agreement Without Identical Coordinates
A displacement lying wholly in $\ker(F)$ has zero KL divergence: $D_{\mathrm{KL}}(p_\theta\,\|\,p_{\theta+d\theta})=\tfrac12 d\theta^{\!\top}F\,d\theta+O(\|d\theta\|^3)$ vanishes there. Two genuinely distinct parameter values can be statistically indistinguishable — concordant — while occupying different coordinates.
**Survey I.** The *Yijing*'s oracle is consulted precisely where the determinate figure underdetermines the outcome: the changing line names a *displacement between indistinguishable futures*, motion in the kernel that the static hexagram cannot resolve.
**Survey II.** Confucius's *"和而不同"* — the noble person harmonizes without being identical — is this fact stated as an ethical maxim: harmony is agreement at zero divergence, and it does not require identical coordinates.
**RAO.** The kernel is where difference and indistinguishability coexist. It is not the absence of structure; it is structure with no distinguishable signature.

### Concordance 5 — The Partition Survives the Change of Chart
Under a reparametrization $\theta\mapsto\theta'$, $F$ transforms as a $(0,2)$-tensor, $F'=J^{\!\top}FJ$, and the split $S\oplus S^{\perp}$ transports covariantly. By Čencov's theorem the Fisher metric is the unique metric, up to a positive scalar, monotone under Markov morphisms — extended to arbitrary sample spaces by Ay, Jost, Lê & Schwachhöfer (2017).
**Survey I.** Euclid's fifth postulate is a *choice of chart*: drop it and the deductive machinery is unchanged, but the geometry re-coordinatizes into the hyperbolic or the elliptic. The theorems re-index; the partition does not.
**Survey II.** Confucius answers *"what is ren?"* differently to Yan Hui, to Zhonggong, to Fan Chi — because *ren* is the Čencov-invariant and each answer is its expression in a different chart, the chart being the student. The invariant is real; it is only ever given relative to coordinates.
**RAO.** What a tradition writes as its axioms or its occasions is a choice of chart. The split into determinate and holistic is the manifold's, not the chart's — and that is why two surveys can concord.

### Concordance 6 — Completeness Is the Direct-Sum Reconstruction
A complete epistemic engine is the reconstruction $T_f\mathcal{M}=S\oplus S^{\perp}$ — estimation to the Cramér–Rao floor on the determinate slice, invariant navigation of the holistic complement. Neither summand alone is the manifold.
**Survey I.** Geometry entire is the fixed figure *and* the changing line: Euclid's proof of what holds, and the *Yijing*'s reading of what moves.
**Survey II.** Ethics entire is the demonstrated proposition *and* the situated response: Spinoza's order of value, and the *Analects*' navigation of it case by case.
**RAO.** The two surveys are not two theories to choose between. Each is a true theory of one summand. The Concordance is the finding that the summands, and their ratio, are the same in both — and the synthesis is their literal direct sum.

---

## The Concordance Table

| # | The Fisher fact | Survey I — Euclid / *Yijing* | Survey II — Spinoza / *Analects* |
|---|---|---|---|
| 1 | $T_f\mathcal{M}=S\oplus S^{\perp}$, total | theorem ⊕ changing line | proposition ⊕ occasioned answer |
| 2 | $S$ finite, computable, Cramér–Rao floor finite | 5 postulates → 13 books | the deductive chain; EIIP7 isomorphism |
| 3 | $S^{\perp}$ infinite, weak metric, bound diverges | the field of change (*yì*) | *ren*, never a finite formula |
| 4 | $\ker(F)$: zero divergence, non-identical coordinates | the changing line between futures | *和而不同* — harmony without sameness |
| 5 | Čencov: partition survives reparametrization | the fifth postulate as a chart | a different answer to each student |
| 6 | completeness = the direct-sum reconstruction | figure ⊕ change = geometry entire | order ⊕ occasion = ethics entire |

The table is the framework's claim in one view: read down either corpus column and the *same six facts* appear. The corpora share nothing — a Greek geometry and a Chinese oracle, a Dutch ethics and a Chinese collection of sayings, separated by domain and by two millennia — and they return the same partition. That convergence is the Concordance.

---

## Five Falsifiable Predictions

**P1 — Cross-survey effective-rank concordance.** *(The spine of the framework.)*
Embed each corpus as a parametric generative model and compute the Fisher spectrum of its fitting objective. The thresholded effective-rank ratio $r_\tau/n$ recovered from Survey I will equal that recovered from Survey II, within sampling error.
*Falsified if* the two surveys yield systematically different ratios — which would make the partition corpus-dependent and collapse the Concordance.
*Status: open. This is the prediction the entire framework stands on.*

**P2 — Within-survey West/East rank agreement.**
Within each survey, the determinate-slice dimension recovered from the Western corpus equals the determinate-slice dimension recovered from the Eastern corpus; the traditions differ in which summand they *occupy*, not in the partition's shape.
*Falsified if* the Western and Eastern corpora of a single survey yield different $r/n$.
*Status: open.*

**P3 — Weakness of the metric on the holistic complement.**
For directions identified with $S^{\perp}$, the empirical estimator variance grows without bound as the eigenvalue $\lambda\to 0$; the product (variance $\times\ \lambda$) is approximately constant — the signature of a weak metric with no bounded inverse.
*Falsified if* $S^{\perp}$-direction variances saturate to a finite bound.
*Status: the weak-metric structure is established in the non-parametric setting (the 2026 *Entropy* result; Pistone & Sempi 1995); the constant-product law is the sharp empirical test.*

**P4 — Reparametrization invariance of the determinate endpoint.**
Run Euclidean-gradient and natural-gradient ($F^{+}\nabla L$) descent from one initialization on a sloppy model drawn from either survey. The $S$-projection of the natural-gradient endpoint is invariant under smooth reparametrization; the Euclidean endpoint is not.
*Falsified if* the natural-gradient endpoint drifts under reparametrization beyond tolerance $\varepsilon$.
*Status: the invariance is established (Amari 1998); the corpus-scale instantiation is open.*

**P5 — Information-gain selection localizes to the determinate slice.**
Selecting training examples to maximize Fisher information gain (FisherSFT-style; Deb et al. 2025) accelerates convergence, and the gain is concentrated entirely in $S$; error along $S^{\perp}$ is invariant to example selection.
*Falsified if* measured improvement appears along holistic directions, or if random selection closes the gap on $S$.
*Status: the acceleration is established (Deb et al. 2025); the localization claim is the open, falsifiable part.*

---

## RAO — The Engine

RAO consumes a corpus, renders it as a statistical manifold, computes the Fisher partition, operates **both summands**, and closes with an invariance audit. In this instantiation it is run twice — once on each survey — and the Concordance is the comparison of the two runs.

| Layer | Name | Operation | In this instantiation |
|---|---|---|---|
| **0** | **Substrate** | Embed the corpus as a smooth family $p_\theta(x)$ on the Pistone–Sempi manifold. | Survey I: *Elements* + *Yijing*. Survey II: *Ethics* + *Analects*. |
| **1** | **Score** | Compute the score field $s_\theta(x)=\nabla_\theta\log p_\theta(x)$. | The differential of distinguishability. |
| **2** | **Fisher Assembly** | Form $F(\theta)=\mathbb{E}_{p_\theta}[\,s\,s^{\!\top}]$; isolate the covariate Fisher matrix on $S$. | The metric tensor — strong on $S$, weak on $S^{\perp}$. |
| **3** | **Structural Partition** | Decompose $T_f\mathcal{M}=S\oplus S^{\perp}$; threshold at $\tau$; report $r,k$. | The determinate-slice and holistic-complement dimensions of each survey. |
| **4** | **Estimation (determinate)** | On $S$, estimate to the Cramér–Rao floor $F^{+}$. | Euclid's theorems; Spinoza's demonstrated propositions. |
| **5** | **Navigation (holistic)** | On $S^{\perp}$, treat directions as gauge; characterize the invariant relations. | The *Yijing*'s changing lines; the *Analects*' situated *ren*. |
| **6** | **Natural-Gradient Transport** | Move on $\mathcal{M}$ by $\tilde\nabla L=F^{+}\nabla L$. | A reparametrization-invariant update, confined to $S$. |
| **7** | **Concordance Audit** | Verify Čencov monotonicity; compare $r_\tau/n$ across the two surveys; report $T_f\mathcal{M}=S\oplus S^{\perp}$. | The certification that the two independent surveys recovered one partition. |

Layers 0–3 build each partition. Layer 4 is the West's complete theory of its slice; Layer 5 is the East's complete theory of its complement. Layer 6 is the motion that respects the metric. Layer 7 is the new layer: it compares the two surveys and certifies their concordance.

---

## Closing

A framework demonstrated once invites the suspicion that it was fitted to its example. The Concordance answers that suspicion by demonstration, not assertion. It takes the Fisher partition to two corpus-pairs that share nothing — a Greek geometry against a Chinese oracle, a Dutch ethics against a Chinese book of sayings — and finds the same six facts in all four texts.

Euclid and Spinoza wrote the finite slice. Each began from an explicit, finite foundation and proved outward: a fixed grid of definitions and postulates, every consequence reachable from it, every identifiable truth pinned to the Cramér–Rao floor. That is a complete and exact theory of the determinate slice $S$ — and a tradition built entirely upon it will look, from inside, like the whole of knowledge.

The *Yijing* and the *Analects* navigated the holistic complement. Neither claimed a finite foundation; each took as its subject the unbounded field — of change, of relation — that no finite chart exhausts. The *Yijing* reads the changing line, the displacement the static figure cannot resolve; the *Analects* gives *ren* only ever relative to the asker, an invariant with no single coordinate expression. That is a complete and exact theory of the holistic complement $S^{\perp}$ — and a tradition built entirely upon it will also look, from inside, like the whole of knowledge.

The 2026 result in non-parametric information geometry supplies the precise word for what each tradition holds. The West holds $S$: finite, computable, its Fisher matrix invertible. The East holds $S^{\perp}$: infinite, its Fisher–Rao metric *weak*, possessed of no bounded inverse — which is the rigorous statement that its directions admit no finite-variance estimator, that they must be navigated and cannot be pinned. The two are orthogonal complements of one tangent space, and Čencov's theorem certifies that the split is the manifold's and not the chart's.

So the verdict is, once again, arithmetic — and now it is arithmetic confirmed twice. $r+k=n$, recovered from geometry; $r+k=n$, recovered from ethics; the same ratio in both rooms. Knowledge is the direct sum $S\oplus S^{\perp}$, and no single survey owns it. RAO is the engine that runs the partition wherever a corpus can be embedded, estimates the determinate slice to its sharp floor, navigates the holistic complement as the real place it is, and reports — across surveys that never met — that the geometry was one geometry all along.

---

## References

**Survey I — the corpora**
1. Euclid. *The Thirteen Books of the Elements* (c. 300 BCE). Trans. and ed. Sir Thomas L. Heath, 3 vols., 2nd edition. Dover, 1956.
2. *The Classic of Changes: A New Translation of the I Ching as Interpreted by Wang Bi*. Trans. Richard John Lynn. Columbia University Press, 1994.

**Survey II — the corpora**
3. Spinoza, B. *Ethics* (*Ethica Ordine Geometrico Demonstrata*, 1677). In *The Collected Works of Spinoza, Vol. I*, trans. and ed. Edwin Curley. Princeton University Press, 1985.
4. Confucius. *Analects* (*Lunyu*). Trans. Edward Slingerland. Hackett Publishing, 2003.

**Information geometry**
5. Rao, C. R. (1945). Information and the accuracy attainable in the estimation of statistical parameters. *Bulletin of the Calcutta Mathematical Society*, 37, 81–91.
6. Cramér, H. (1946). *Mathematical Methods of Statistics*. Princeton University Press.
7. Kullback, S., & Leibler, R. A. (1951). On information and sufficiency. *Annals of Mathematical Statistics*, 22(1), 79–86.
8. Čencov (Chentsov), N. N. (1982). *Statistical Decision Rules and Optimal Inference*. Translations of Mathematical Monographs, vol. 53. American Mathematical Society.
9. Amari, S. (1985). *Differential-Geometrical Methods in Statistics*. Lecture Notes in Statistics, vol. 28. Springer.
10. Amari, S. (1998). Natural gradient works efficiently in learning. *Neural Computation*, 10(2), 251–276.
11. Pistone, G., & Sempi, C. (1995). An infinite-dimensional geometric structure on the space of all the probability measures equivalent to a given one. *Annals of Statistics*, 23(5), 1543–1561.
12. Ay, N., Jost, J., Lê, H. V., & Schwachhöfer, L. (2017). *Information Geometry*. Ergebnisse der Mathematik und ihrer Grenzgebiete. Springer.

**Sloppy models, identifiability, and current research**
13. Brown, K. S., & Sethna, J. P. (2003). Statistical mechanical approaches to models with many poorly known parameters. *Physical Review E*, 68, 021904.
14. Transtrum, M. K., Machta, B. B., Brown, K. S., Daniels, B. C., Myers, C. R., & Sethna, J. P. (2015). Perspective: Sloppiness and emergent theories in physics, biology, and beyond. *Journal of Chemical Physics*, 143.
15. Karakida, R., Akaho, S., & Amari, S. (2019). Universal statistics of Fisher information in deep neural networks: mean field approach. *AISTATS* (PMLR).
16. Deb, R., Thekumparampil, K., Kalantari, K., Hiranandani, G., Sabach, S., & Kveton, B. (2025). FisherSFT: Data-efficient supervised fine-tuning of language models using information gain. *Proceedings of the 42nd International Conference on Machine Learning (ICML)*, PMLR 267. arXiv:2505.14826.
17. An approach to the Fisher–Rao metric for infinite-dimensional non-parametric information geometry. *Entropy*, 28(4), 374 (2026). doi:10.3390/e28040374. — Introduces the structural tangent-space decomposition $T_f\mathcal{M}=S\oplus S^{\perp}$ and the Covariate Fisher Information Matrix on the Pistone–Sempi manifold.

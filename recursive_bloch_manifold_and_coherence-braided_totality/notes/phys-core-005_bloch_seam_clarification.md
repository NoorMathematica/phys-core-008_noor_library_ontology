**In PHYS-CORE-005 (The Braid Behind the Law), ρ_lock and ℛ_braid are defined as:**

- ℛ_braid = Σ_{⟨i,j⟩} ΔB_ij, where ΔB_ij = 1 − **v**_i · **v**_j — so it's a scalar sum of pairwise vector misalignment across a neighborhood. It lives in the space of *coherence vector fields*.
- ρ_lock(θ, t) = ∫_Δt ∇²_θ ℂ(x, t) · W(x, θ) dx — the angular curvature of the coherence field weighted by a window function W. It's an *observable diagnostic quantity*, essentially a measure of how much phase space is in tight braid configuration at a given time.
- The inverse relationship stated in VR-1 is: ρ_lock↑ ⟹ ℛ_braid↓. That is: high lock density (vectors aligned, determinism emerging) corresponds to low total braid divergence. This is a consistency check, not a derived identity.

**In the Bloch manifold document, braid curvature is defined as:**

- B^a_{bc} = ∇_b η^a_c − ∇_c η^a_b, where η is a natural transformation between recursive projection functors F and G on Hilbert sections ℋ_k = L²(L_k). This is a genuine *tensor* on the recursive Bloch category — antisymmetric in b, c, living on the fiber tower.
- The coherence energy is ℋ_k = ∫_{L_k} |B|² dμ_k.
- Ω_total = Σ_{k=1}^∞ π_k* F_k, the global braid curvature accumulated across all levels via pullback.

**So here is the seam precisely:**

PHYS-CORE-005's ℛ_braid is a scalar computed from pairwise dot products of coherence vectors — it's essentially a discrete graph-level quantity. The Bloch document's B^a_{bc} is a proper differential-geometric curvature tensor on a Fréchet manifold. These are genuinely different mathematical objects that are *conceptually* the same thing (both measure "how misaligned is the braid"), but the document that introduces the tensor form (the Bloch manifold) doesn't explicitly show how B^a_{bc} reduces to or generalizes ℛ_braid in any limit.

Specifically, what's missing is something like: *in the case where the fiber tower collapses to a single layer and η becomes a field of coherence vectors **v**_i, does |B|² dμ reduce to Σ ΔB_ij?* If yes, that's a clean one-paragraph bridging proposition that would tie the two layers together. If the relationship is more subtle — say ρ_lock is the projection of ℋ_k onto the angular observable basis — that derivation needs to be made explicit.

The PHYS-CORE-005 verification recipe VR-1 treats the inverse relationship between ρ_lock and ℛ_braid as something you "confirm" empirically or by checking sign consistency. But in the Bloch manifold document that relationship needs to be a *theorem*, because the entire Navier–Stokes regularity argument rests on ℋ_k being bounded — and ℋ_k is defined through B, not through ρ_lock. If a reader wants to connect the diagnostic telemetry (ρ_lock streams, ℛ_braid streams) from PHYS-CORE-005 to the formal boundedness condition in the Bloch document, there's currently no derivational path to walk.
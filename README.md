Title (Preprint: DOI:https://doi.org/10.21203/rs.3.rs-10615527/v1)

Persistence-Weighted Descriptors: A Topologically Stable Local Feature Representation for Deformation-Robust Image Matching

Abstract

Local feature descriptors underpin correspondence estimation across computer vision, yet virtually all widely-used descriptors — handcrafted or learned — are built from raw or gradient-transformed pixel intensities whose stability under perturbation is established only empirically, not proven. This matters most where a correspondence error is costly and an auditable guarantee is part of the deliverable: medical registration, forensic analysis, and safety-relevant settings, not general-purpose matching. We introduce PW-Desc (Persistence-Weighted Descriptor) for this niche: a local descriptor built from the sublevel-set persistent homology of a multi-scale patch, prioritizing a proved stability bound over state-of-the-art accuracy. Persistence diagrams admit a classical Lipschitz stability guarantee (Cohen-Steiner, Edelsbrunner and Harer, 2007); we prove this survives our vectorization and projection stages under a spectral-norm constraint, and separately prove an exact invariance guarantee for a rank-normalized variant, PW-Desc-rank, under monotonic photometric transforms. The pipeline is implemented from scratch, cross-validated bit-for-bit against GUDHI C++. We report measured results including three real benchmarks (Oxford-Affine, HPatches, MegaDepth, 660 pairs) and real comparisons against official SuperPoint, DISK, and LoFTR checkpoints: PW-Desc trails every one of them in raw accuracy (significant throughout), while PW-Desc-rank consistently beats plain PW-Desc, consistent with the proof. Further CPU-only results — correctness checks, stress tests, a detector ablation, and runtime optimizations narrowing the gap to classical descriptors — are reported the same way. Only ScanNet remains outstanding among the four named benchmarks, blocked by a Terms-of-Use approval process rather than technical access. Code, proofs, and reproduction commands are released publicly.

(240 words, source-counted, under Discover Computer Vision's 250-word limit)

Keywords

local feature descriptors, persistent homology, topological data analysis, image matching, deformation robustness, stability theory

***Paper submitted to the Journal of Mathematical Imaging and Vision.

Title

Persistence Weighted Image Descriptors with Certified Stability Bounds under Intensity Perturbations and Exact Monotone Invariance

Abstract

Local descriptors decide which correspondences reach a registration pipeline, yet none of the common ones has a proved bound on its response to intensity perturbations. We build a descriptor from the cubical persistent homology of patches and carry the bottleneck stability theorem through vectorization, normalization and a learned projection with explicit constants. A rank-normalized variant is exactly invariant to strictly increasing intensity transforms. A second bound, valid when short-lived features get zero weight, depends only on the clean patch and is up to 17 times smaller, and we prove that the number of diagram points in such bounds cannot be removed. On real photographs all 158,400 individual inequality checks hold, while the bounds stay two to three orders of magnitude above the observed change. In Monte Carlo registration the descriptor fails more often than SIFT under strong noise and blur, while the rank variant is exact under gamma changes.

Keywords

persistent homology; stability theorem; persistence images; local image descriptors; image registration; topological data analysis

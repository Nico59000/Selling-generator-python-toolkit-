# Selling Toolkit v0.4.3

Exact, replayable Python toolkit extracted from the v0.4 Selling research line.

Current public modules:
- `selling_toolkit.layers`: exact v54 layer classification, canonical deck/relabel/sign quotient, Tarjan SCC;
- `selling_toolkit.fast_layers`: exact integer canonical index with explicit `int64` overflow guard and SymPy-oracle regression path;
- `selling_toolkit.quartic`: Pascal-reduced ternary quartic reconstruction, exact v54 `rho`, GL3 covariance and explicit quartic reconstruction on a supplied GL3(Q) orbit;
- `selling_toolkit.rational_forms`: exact rational congruence diagonalization, determinant square classes, local Hilbert/Hasse invariants, Hasse–Minkowski decision, unbounded constructive exact witness construction on the rationally isotropic ternary branch, and fixed-scale quartic-covariance orbit testing;
- `selling_toolkit.extension`: guarded 3D+2D -> 5D lifts.

The 5D layer now distinguishes three levels:
1. `ProductLift3D5D`: typed product carrier only;
2. `TrivialSellingLift3D5D`: passive fibre `diag(A3,I2)`;
3. `DeterminantSwapSellingLift3D5D`: exact non-passive fibre representation induced by `sign(det A3)`, with orientation-reversing Selling steps swapping the two fibre coordinates;
4. `GoldenResidualFibreAdapter`: exact intertwiner from signed residuals to the positive golden residual fibre, with `J Gamma_phi(r)=Gamma_phi(-r)` and `Delta Gamma_phi(r)=r`;
5. `CoboundaryCoupledSellingLift3D5D`: an explicit `C != 0` source-exact lower-triangular lift, proved conjugate to the determinant-swap lift and therefore gauge-trivial rather than a new native 5D wall theory.

The determinant-swap lift is an exact algebraic representation of the current Selling transformation source on an ordered positive two-coordinate fibre. v0.4.3 supplies an explicit adapter to the historical **golden residual** fibre only. The full Binet/elliptic/deck carriers remain separated. The nonzero-C construction is a coboundary/conjugate lift, so a genuinely new native 5D wall/conorm reduction theory remains open.

For rational ternary quadratic forms, Hasse–Minkowski decides rational congruence. The toolkit separately checks the stronger fixed-scale quartic covariance condition

`det(Q_target)/det(Q_base) = det(A)^16`,

so ordinary rational congruence is never silently promoted to a quartic-covariance reconstruction.


The v0.4.3 exact ternary witness path clears denominators and invokes an exact homogeneous ternary-quadratic Diophantine solver; there is no user-supplied vector search bound. Every returned isotropic vector and every congruence matrix is replayed by exact rational matrix equality.

# Selling Toolkit v0.4.4

Exact, replayable Python toolkit extracted from the v0.4 Selling research line.

Current public modules:
- `selling_toolkit.layers`: exact v54 layer classification, canonical deck/relabel/sign quotient, Tarjan SCC;
- `selling_toolkit.fast_layers`: exact integer canonical index with explicit `int64` overflow guard and SymPy-oracle regression path;
- `selling_toolkit.quartic`: Pascal-reduced ternary quartic reconstruction, exact v54 `rho`, GL3 covariance and explicit quartic reconstruction on a supplied GL3(Q) orbit;
- `selling_toolkit.rational_forms`: exact rational congruence diagonalization, determinant square classes, local Hilbert/Hasse invariants, Hasse–Minkowski decision, unbounded constructive exact witness construction on the rationally isotropic ternary branch, and fixed-scale quartic-covariance orbit testing;
- `selling_toolkit.extension`: guarded 3D+2D -> 5D lifts.

The 5D layer now distinguishes three levels:
1. `ProductLift3D5D`: typed product carrier only;
2. `TrivialSellingLift3D5D`: passive fibre `diag(A3,I2)`;
3. `DeterminantSwapSellingLift3D5D`: exact non-passive fibre representation induced by `sign(det A3)`, with orientation-reversing Selling steps swapping the two fibre coordinates;
4. `GoldenResidualFibreAdapter`: exact intertwiner from signed residuals to the positive golden residual fibre, with `J Gamma_phi(r)=Gamma_phi(-r)` and `Delta Gamma_phi(r)=r`;
5. `CoboundaryCoupledSellingLift3D5D`: an explicit `C != 0` source-exact lower-triangular lift, proved conjugate to the determinant-swap lift and therefore gauge-trivial rather than a new native 5D wall theory.

The determinant-swap lift is an exact algebraic representation of the current Selling transformation source on an ordered positive two-coordinate fibre. v0.4.3 supplies an explicit adapter to the historical **golden residual** fibre only. The full Binet/elliptic/deck carriers remain separated. The nonzero-C construction is a coboundary/conjugate lift, so a genuinely new native 5D wall/conorm reduction theory remains open.

For rational ternary quadratic forms, Hasse–Minkowski decides rational congruence. The toolkit separately checks the stronger fixed-scale quartic covariance condition

`det(Q_target)/det(Q_base) = det(A)^16`,

so ordinary rational congruence is never silently promoted to a quartic-covariance reconstruction.


The v0.4.4 exact ternary witness path clears denominators and invokes an exact homogeneous ternary-quadratic Diophantine solver; there is no user-supplied vector search bound. Every returned isotropic vector and every congruence matrix is replayed by exact rational matrix equality.


## v0.4.4 determinant-swap H1 no-go

`selling_toolkit.cohomology.DeterminantSwapH1NoGo` certifies that every source-exact linear lower-triangular coupling `C(A)` for the determinant-swap fibre module is a coboundary. A finite subset of exact matrix relations already gives generator-level cocycle solution dimension 6, equal to the 6-dimensional coboundary space, hence actual `H^1` is zero. The relation list is not claimed to be a complete presentation; it is sufficient for the no-go. Nonlinear extensions, different fibre representations, and genuinely native 5D Selling walls/conorms remain open.

## v0.4.5 continuation-11

- Public-schema stability pass 1/2: all 0.4.4 exports/signatures and critical numeric/quartic/CLI modules preserved byte-for-byte.
- Adds exact `GoldenResidualAffineH1NoGo`: affine signed-residual shifts have H^1=0 under the sufficient exact Selling relation set, hence are gauge-trivial.
- Existing det-swap linear H^1=0, golden residual adapter, exact quartic inverse and fast integer quotient APIs remain unchanged.

## v0.4.6 additive fibre-representation audit

Adds `BaseModuleRank2FibreNoGo`: the six exact Selling wall matrices generate all of `M_3(Q)` (dimension 9), hence the source base module `Q^3` is irreducible. No natural rank-2 fibre can therefore be obtained as a linear subrepresentation or quotient of that base module. This is a scoped no-go; unrelated 2D representations, nonlinear/finite fibres and native 5D walls/conorms remain open (a track oppened on $$\boxed{
C_3\hookrightarrow S_3,
}$$) . Existing public APIs and CLI are unchanged.

v55 progression on Binet Birefringence produced : see the latex-equation2.pdf joined

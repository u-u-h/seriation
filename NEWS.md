# Changes in version 1.2-1.1 (xx/x/2016)

* Criterion: dist objects are now automatically converted into a  
  similarity matrix for ME, Moore\_stress and Neumann\_stress.
* Added criterion Cor_R (ME for the moment ordering algorithm by 
  Deutsch and Martin)
* pimage now supresses the color key for logical matrices and checks for
  all NAs and infinite entries.

# Changes in version 1.2-1 (08/06/2016)

* The default setting for ser_dist and ser_cor is now reverse is TRUE.
* Bugfix: pimage did now work with matrices containing only a single value.
* Bugfix: control parameters for method TSP are now correctly passed on
  (reported by David Aliyev)
* Added new distance measure called absolute pairwise rank differences.

# Changes in version 1.2-0 (2/22/2016)

* Fixed RGAR (w needs to be in [2,n-1]).
* RGAR gained parameter pct to specify the window as a percentage.
* Added the lazy path length criterion.
* Added the banded anti-Robinson form (BAR) criterion.
* Added QAP_Inertia and QAP_BAR solver.
* Added DendSer using register_DendSer().
* Added GA using register_GA().
* Registry now warns and modifies entries with the same name.
* Registry now lists methods in alphabetical order.
* Seriation method alias Chen was removed. Use R2E.

# Changes in version 1.1-3 (12/18/2015)

* Added is.robinson to recognize (pre) Robinson matrices.
* Added random.robinson to create random Robinson matrices.
* Added seriation methods "QAP_LS" and "QAP_2SUM" (QAP-based seriation).
* Added criteria "LS" and "2SUM" from QAP-based seriation.
* Fixed Spectral_norm seriation.
* hmap now honors zlim also in dendrogram-based maps.
* hmap gained option sym for seriation based maps. showdist can now be
      one of "none" (default), "row", "column", or "both".
* ser_cor and ser_dist gained parameter y. ser_cor gained parameter test
      to perform tests for association.
* Added permute method for hclust and dendrogram objects.

# Changes in version 1.1-2 (8/23/2015)

* Argument (control and ...) check warns now instead of throwing an error.
* seriation_dist, seriation_cor and seriation_align are now shortened to
      ser_dist, ser_cor and ser_align.
* Method "ppc" is now faster and also available in ser_cor.
* Fixed ser_cor for "spearman" and "Kendall" (uses now rank correctly).
* ser_cor and ser_dist gained parameter reverse to indicate that
        permuations are also tried in reverse and the best value is reported.

# Changes in version 1.1-1 (7/1/2015)

* get_permutation_matrix added.
* seriation_dist measure "ppc" (positional proximity coefficient) added.
* Fixed bug with permute and ser_permutation_vectors.
* Identity permutations (NA) give now an error for get_order and
        get_permutation_matrix.
* Fixed imports for non-base R packages.

# Changes in version 1.1-0 (06/09/2015)

* Seriation method 'Identity' added.
* Seriation method 'Random' added.
* Seriation method 'VAT' added.
* Seriation methods 'Spectral' and 'Spectral_norm' added.
* Seriation methods 'PCA_angle' and 'MDS_angle' added.
* Seriation methods 'SPIN_NH' and 'SPIN_STS' added.
* Several aliases for seriation methods added.
* Criterion 'RWGAR' added.
* permutation_matrix2vector and permutation_vector2matrix added.
* Identity permutation (value NA) added.
* ser_permutation and ser_permutation_vector can now be used interchangably,
* get_rank for permutation vectors added.
* seriation_dist and seriation_alignment to calculate
        dissimilarities between seriation orders added.
* Wood data set added.
* # Chameleon data sets added.
* create_lines_data, create_ordered_data added.
* pimage, hmap and dissplot: Simplified and made interfaces more
        consistent (all use now zlim, consistent default color palettes).
* pimage gained axes and prop; NA in matrix now works.
* seriation checks now control arguments consistently.
* We use now package registry to manage methods.
* reorder for hclust added.
* iVAT with path distance added.
* color palettes (bluered, greenred, greys) added.
* Improved speed of C code.
* Fixed problem with testthat filenames fixed.
* bburg.f/bbwrg.f: memory access problem fixed.

# Changes in version 1.0-14 (12/02/2014)

* arsa.f: removed 0 flag in rand() so it compiles under AIX
      (reported by Lei Zhang)
* arsa.f/bburg.f/bbwrg.f: calls now R RNG to be compatible with certain
	    compilers (e.g., Intel FORTRAN) (reported by Rohan Shah)

# Changes in version 1.0-13 (3/11/2014)

* Fixed dependence on MASS

# Changes in version 1.0-12 (2/18/2014)

* ser_permutation_vectors can now be reversed with rev
* get_order: removed the weird labels.
* we use now testthat
* fixed bug with intra-cluster ordering using silhouette width
	    (reported by Bettina Gruen)
* Cleaned up dependencies: TSP, grid, cluster, gclus and colorspace are
	    now imports instead of dependencies.

# Changes in version 1.0-11 (9/6/2013)

* service release.

# Changes in version 1.0-10 (2/15/2013)

* pimage has now a colorkey and a range argument
* fixed bug in ARSA when the distance matrix contains all 0s
* added PACKAGE argument to .Fortran calls

# Changes in version 1.0-8 and 1.0-9 (11/6/2012)

* get_order: labels are now in the correct order (Bug report by Crt Ahlin)
* Replaced Fortran I/O with R I/O for verb=TRUE
* Fixed pop/newpage bug in pimage.dist (reported by Bettina Gruen)

# Changes in version 1.0-7 (9/25/2012)

* Fixed out-of-bounds bug in arsa.f (reported by Rohan Shah)
* Fixed out-of-bounds bug in bburcg.f

# Changes in version 1.0-6 (10/19/2011)

* removed deprecated parameter gamma for dissplot()

# Changes in version 1.0-5 (9/2/2011)

* bertinplot(): fixed representation for 0, neg. values and highlight.
	    (Bug report by G. Sawitzki).
* bertinplot(): added panel.blocks and option for shading
* bertinplot(): added bertin_cut_line()

# Changes in version 1.0-4 (6/28/2011)

* pimage() now uses grid.raster.
* dissplot() now uses grid.raster.

# Changes in version 1.0-3 (1/14/2011)

* improved validity check for permutations and added check for dist with
	    neg. entries to seriate.dist.

# Changes in version 1.0-2 (3/13/2010)

* service release

# Changes in version 1.0-1 (8/25/2009)

* added drop=FALSE in permute for matrix.
* fixed reordering for labels.
* added permute for character.
* added different methods to calculate between cluster
	    dissimilarities (min, max, avg, Hausdorff).
* dissplot has now additional options hue, power, gamma, flip and
	    changed behavior for averages. dissplot depends now on colorspace.

# Version 1.0-0 (3/24/2009)

# Version 0.1-1 (9/1/2007)

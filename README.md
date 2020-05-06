# SysSimDataInputs
The SysSimDataInputs repository should be automatically installed as a submodule of SysSimData (https://github.com/ExoJulia/SysSimData) in a directory named inputs.
This repository contains (mostly) text data to be used by [SysSim](https://github.com/ExoJulia/ExoplanetsSysSim.jl).
In some cases these files may be read directly, but often it will be converted into a binary file to be stored in the main data directory.

## Files
- KeplerMAST_TargetProperties.csv: Which stars were observed which quarters as part of Kepler planet search (symlink to inputs/KeplerMAST_TargetProperties.csv)
- Gaia_Kepler_2MASS_mags.csv: 2MASS magnitudes for 1" cross-referenced targets between Kepler DR25 and Gaia DR2
- q1_q17_dr25_koi.csv: Kepler planet candidate properties as tabulated in DR25 catalog
- q1_q17_dr24_koi.csv: Old Kepler planet candidate properties as tabulated in DR24 catalog (may be useful for comparison purposes)
- q1_q12_koi.csv: Old catalog Kepler planet candidate properties (may be useful for comparison purposes)
- q1_q16_koi.csv:  Old catalog Kepler planet candidate properties (may be useful for comparison purposes)

## Files not directly in the repository
There are a few larger csv files that aren't included directly, but can be downloaded separately by running 'julia scripts/make.jl --download-stellar-catalog' from the SysSimData directory (typically named data) if you want the CSV files for the stellar catalogs.
- q1_q17_dr24_stellar.csv: Kepler planet candidate properties as tabulated in DR24 catalog (symlink to inputs/q1_q17_dr24_koi.csv)
- q1_q17_dr25_stellar.csv: Kepler planet candidate properties as tabulated in DR25 catalog (symlink to inputs/q1_q17_dr25_koi.csv)

Inputs files that are only in the SysSimData (https://github.com/ExoJulia/SysSimData) repository/data directory due to their size.
- dr25_koi_mcmc_quant.csv: Quantiles for transit depths and durations computed from MCMC posterior samples
- DR25topwinfuncs.jld2: Window functions that cover nearly all the Kepler planet search targets
- KeplerMAST_TargetProperties.jld2: Binary version of inputs/KeplerMAST_TargetProperties.csv
- dr25fgk_relaxcut_osds.jld2: One-sigma depth functions for healthy subset of Kepler planet search targets.  To be downloaded into data directory with 'julia scripts/make.jl --download-stellar-catalog'.
- allosds.jld2: One-sigma depth functions for all Kepler planet search targets.  Optional file that can be downloaded into data directory with 'julia scripts/make.jl --download-stellar-catalog --download-large-files'.

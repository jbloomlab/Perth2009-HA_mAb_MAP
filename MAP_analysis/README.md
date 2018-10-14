# Mutational antigenic profiling of Perth/2009 H3 with human monoclonal antibodies

This directory contains analysis of monoclonal antibody selections of A/Perth/16/2009 (H3N2) HA mutant viruses.

This work was performed and analyzed by Juhye Lee and Jesse Bloom. This project is in collaboration with Seth Zost and Scott Hensley.

Briefly, this analysis maps escape mutations in the Perth/2009 H3 HA from monoclonal antibodies isolated from humans vaccinated with the Victoria/2009 (H3N2) strain.

## Organization

The analysis is performed by the Jupyter notebook [analysis_notebook.ipynb](analysis_notebook.ipynb) using the [dms_tools2](https://jbloomlab.github.io/dms_tools2/) software. This notebook contains the computer code and describes the results.

All generated results are placed into the [./results/](./results/) directory.
All necessary input files are located int the [./data/](./data/) directory.

### Subdirectory organization

The [./data/](./data/) contains the following input items:

  * [./data/H3renumbering_scheme.csv](./data/H3renumbering_scheme.csv): `CSV` file that allows conversion from sequential numbering (1, 2, 3,... etc.) to H3 numbering.
  * [./data/Perth09_HA_reference.fa](./data/Perth09_HA_reference.fa): contains the wildtype sequence of the A/Perth/16/2009 (H3N2) HA used for these experiments.
  * [./data/samples.csv](./data/samples.csv): `CSV` file that lists the samples, the SRA run the contains the deep sequencing data for each sample, and other sample metadata.
  * [./data/summary_avgprefs_rescaled_H3num.csv](./data/summary_avgprefs_rescaled_H3num.csv): the across-replicate averaged and rescaled amino-acid preferences for the Perth/2009 HA mutant libraries generated with a helper virus, in H3 numbering. Taken from [Lee, et al.](http://www.pnas.org/content/early/2018/08/10/1806133115)
  * [./data/wildtypeoverlayfile.csv](./data/wildtypeoverlayfile.csv): `CSV` file listing the wildtype am.ino acids for every site of the Perth/2009 H3.
  

The [./results/](./results/) directory contains the following subdirectories (all other subdirectories are included in the `.gitignore`):
  * [./results/renumberedcounts/](./results/renumberedcounts/): contains codon counts of each sample in H3 numbering as a `csv` file.
  * [./results/differential_selections/](./results/differential_selections/): contains the differential selection values of each sample, in `csv` files. Also contains the logo plots for the entire gene for each sample and the averaged samples.
  * [./results/plots/](./results/plots/): contains the zoomed logo plots in `pdf` format.
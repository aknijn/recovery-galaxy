# recovery-galaxy
A user-friendly and sequencing platform-independent bioinformatics pipeline to build SARS-CoV-2 complete genomes from raw sequencing reads and to investigate variants.   The pipeline is implemented as a Galaxy (https://galaxyproject.org/) workflow. 

The file Galaxy-Workflow-RECoVERY.ga contains the Galaxy workflow that can be imported into any Galaxy instance.  

The tools folder contains the personalised tools and data that the pipeline uses. You can copy the content of the folder to a folder name RECoVERY to the tools folder of your Galaxy instance and add the following lines to the tool_conf.xml file to activate them.
```
<section id="recovery" name="RECoVERY">
  <tool file="RECoVERY/ivar_variants_to_vcf.xml" />
  <tool file="RECoVERY/ivar_covid_aries_consensus.xml" />
  <tool file="RECoVERY/ivar_covid_variants.xml" />
  <tool file="RECoVERY/remove_aa_artifact.xml" />
  <tool file="RECoVERY/blast_to_fasta.xml" />
  <tool file="RECoVERY/sars-cov-2_3.1-genomes.xml" />
  <tool file="RECoVERY/pangolin_3.x.xml" />
</section>
```
The other tools can be installed directly from the Galaxy Toolshed:
*  SnpEff https://toolshed.g2.bx.psu.edu/repository?repository_id=93a5efea7e957b53

*  NCBI BLAST+ https://toolshed.g2.bx.psu.edu/repository?repository_id=1d92ebdf7e8d466c

*  QualiMap BamQC https://toolshed.g2.bx.psu.edu/repository?repository_id=d33f3da25bc5e2f2


A preprint of RECoVERY is available at: https://doi.org/10.1101/2021.01.16.425365

![flow chart of the tool](https://github.com/aknijn/recovery-galaxy/blob/master/sars-cov-2-recovery.png?raw=true)




 **Malaria Resistance Genomics Dashboard for Africa**

 **Project Overview**
This project analyzes *Plasmodium falciparum* genomic data to detect **artemisinin resistance mutations**, with a focus on African isolates.  
We build a **bioinformatics pipeline** for variant calling and annotation, and present results in an interactive **dashboard** that highlights resistance hotspots across Africa.  

 **Objectives**
- Detect mutations in **kelch13** and other drug resistance loci.
- Summarize resistance mutation frequencies by region.
- Provide an **interactive visualization dashboard** for researchers and public health stakeholders.

 **Motivation**
Malaria remains a leading cause of illness and death in sub-Saharan Africa. Artemisinin is the frontline drug for malaria treatment, but resistance is spreading.  
By tracking resistance mutations, this project contributes to understanding **drug resistance trends** and supports **public health decision-making**.

 **Methods & Pipeline**
The pipeline follows these steps:

1. **Data Collection**
   - Reference genome & annotation: [PlasmoDB](https://plasmodb.org/)
   - Sequencing data: [MalariaGEN P. falciparum Project](https://www.malariagen.net/projects/pf)

2. **Preprocessing**
   - Alignment: `BWA → SAMtools`
   - Sorting & indexing BAM files

3. **Variant Calling**
   - Variant calling: `bcftools`
   - Multi-sample VCF generation

4. **Variant Annotation**
   - Annotated with **SnpEff**
   - Focus on **kelch13** mutations (C580Y, R539T, Y493H, etc.)

5. **Resistance Analysis**
   - Frequency analysis per country/region
   - Link to metadata (location, year)

6. **Visualization Dashboard**
   - Built with **Streamlit**
   - Includes:
     - Bar chart of mutations per country
     - Map of resistance hotspots

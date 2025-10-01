# CAP5510 Project Proposal: Genome Assembly Algorithm Comparison

## Team Members
- Vishnu Vivek Valeti (UFID: 44729768)  
- Durga Mahesh Boppani (UFID: 90679845)  
- Venkata Satya Dinesh Chandra Gupta Kolipakula Dhatri (UFID: 79236303)  

## Abstract
Genome assembly is a fundamental task in bioinformatics that reconstructs complete genomes from short sequencing reads. Numerous assembly algorithms exist, each offering distinct strengths and limitations in terms of accuracy, contiguity, and computational performance. This project proposes a comparative analysis of three widely used assemblers—SPAdes, Velvet, and SOAPdenovo—using bacterial genome sequencing datasets. Assemblies will be evaluated on standard quality metrics such as N50, total assembly length, number of contigs, and genome coverage, alongside runtime and memory usage. The results will highlight trade-offs between assembly quality and computational efficiency, providing practical insights for selecting appropriate tools in microbial genomics.

## Background
Next-generation sequencing (NGS) technologies have enabled rapid and cost-effective genome sequencing, producing large volumes of short reads. Assembling these reads into complete genomes remains a challenging computational problem, directly impacting downstream applications such as genome annotation, comparative genomics, and evolutionary studies.

Several assemblers have been developed using de Bruijn graph approaches, each with unique strategies:

- **SPAdes**: Employs multi-k-mer strategies optimized for microbial genomes, typically producing high-quality assemblies.  
- **Velvet**: One of the first efficient de Bruijn graph assemblers, known for its speed and simplicity.  
- **SOAPdenovo**: Designed for large and complex genomes, offering scalability but requiring careful parameter tuning.  

Comparing these assemblers on identical datasets will allow us to assess how algorithmic design choices affect assembly outcomes and resource demands.

## Objectives
1. Install and configure SPAdes, Velvet, and SOAPdenovo.  
2. Assemble bacterial genomes using selected Illumina sequencing datasets.  
3. Evaluate assembly quality using metrics such as N50, total length, number of contigs, and genome coverage.  
4. Measure computational performance including runtime and memory usage.  
5. Analyze trade-offs and provide recommendations for assembler selection.  

## Methodology
1. **Dataset Selection**  
   - Obtain Illumina sequencing datasets for bacterial genomes from the NCBI Sequence Read Archive (SRA).  
   - Example datasets:  
     - *Escherichia coli K-12 MG1655*: [SRR1770413](https://www.ncbi.nlm.nih.gov/sra/?term=SRR1770413)  
     - *Bacillus subtilis subsp. subtilis 168*: [SRR12519857](https://www.ncbi.nlm.nih.gov/sra/?term=SRR12519857)  
   - Select datasets with varying read lengths and coverage to assess robustness.  

2. **Assembly Process**  
   - Run assemblies with default parameters for each tool.  
   - Record results and optionally test parameter variations (e.g., k-mer size).  

3. **Evaluation**  
   - Use QUAST to compute assembly statistics (N50, contig count, genome coverage, total length).  
   - Profile runtime and memory usage using Linux system utilities.  

4. **Comparison and Analysis**  
   - Summarize results in comparative tables and plots.  
   - Identify strengths and weaknesses of each assembler.  
   - Discuss trade-offs between assembly quality and efficiency.  

## Tools and Datasets
- **Assemblers**: SPAdes, Velvet, SOAPdenovo  
- **Datasets**: Illumina bacterial genome datasets from NCBI SRA (e.g., [E. coli K-12 MG1655 SRR1770413](https://www.ncbi.nlm.nih.gov/sra/?term=SRR1770413), [B. subtilis SRR12519857](https://www.ncbi.nlm.nih.gov/sra/?term=SRR12519857))  
- **Evaluation Tools**: QUAST, Linux profiling utilities (time, memory)  
- **Environment**: Linux-based systems; Python/R for result visualization  

## Expected Results
- A quantitative comparison of the three assemblers across multiple performance metrics.  
- Clear insights into tool strengths: SPAdes for high-quality assemblies, Velvet for speed, SOAPdenovo for scalability.  
- Visualized trade-offs between assembly accuracy and computational efficiency.  
- A final report summarizing findings and recommendations for assembler use in microbial genome assembly tasks.  

## Workload Distribution
- **Vishnu Vivek Valeti**: Setup of assemblers (SPAdes, Velvet, SOAPdenovo), documentation.  
- **Durga Mahesh Boppani**: Dataset collection from NCBI SRA, execution of initial assembly runs.  
- **Venkata Satya Dinesh Chandra Gupta Kolipakula Dhatri**: Assembly evaluation with QUAST, analysis of results, visualization of findings.  

## References
1. Bankevich A. et al. (2012). SPAdes: A New Genome Assembly Algorithm and Its Applications to Single-Cell Sequencing. *Journal of Computational Biology.*  
2. Zerbino D. R., Birney E. (2008). Velvet: Algorithms for de novo short read assembly using de Bruijn graphs. *Genome Research.*  
3. Luo R. et al. (2012). SOAPdenovo2: An empirically improved memory-efficient short-read de novo assembler. *GigaScience.*  
4. Gurevich A. et al. (2013). QUAST: quality assessment tool for genome assemblies. *Bioinformatics.*  

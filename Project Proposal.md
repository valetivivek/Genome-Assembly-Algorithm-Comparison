# Project Proposal: Genome Assembly Algorithm Comparison

## Team Members
- Vishnu Vivek Valeti  
- Durga Mahesh Boppani  
- Venkata Satya Dinesh Chandra Gupta Kolipakula Dhatri  

## Abstract
Genome assembly is a fundamental task in bioinformatics that reconstructs whole genomes from short sequencing reads. Numerous assembly algorithms have been developed, each with distinct advantages and trade-offs in contiguity, accuracy, and computational efficiency. This project proposes a comparative evaluation of three widely used assemblers—SPAdes, Velvet, and SOAPdenovo—using bacterial genome sequencing datasets. The assemblers will be benchmarked on performance metrics including N50, total assembly length, number of contigs, genome coverage, runtime, and memory usage. The findings are expected to provide practical insights into the trade-offs between assembly quality and computational resources, offering recommendations for tool selection in microbial genome assembly workflows.

## Background
High-throughput sequencing technologies have revolutionized genomics by enabling the rapid generation of large volumes of short sequencing reads. However, assembling these reads into accurate and contiguous genomes remains a computational challenge. Efficient genome assembly is essential for downstream applications such as genome annotation, phylogenetic studies, and comparative genomics.

Several notable algorithms exist for de novo genome assembly:

- **SPAdes**: A multi-k-mer assembler optimized for microbial genomes, known for producing high-quality assemblies.  
- **Velvet**: One of the earliest de Bruijn graph-based assemblers, valued for its speed and efficiency.  
- **SOAPdenovo**: Designed for large-scale genomes, offering scalability but requiring careful parameter tuning.  

These assemblers adopt different strategies for read error correction, graph construction, and scaffolding. A systematic comparison on common datasets will highlight how these differences affect assembly quality and computational performance.

## Objectives
1. Install and configure SPAdes, Velvet, and SOAPdenovo.  
2. Perform genome assembly on selected bacterial sequencing datasets.  
3. Evaluate assemblies using metrics such as N50, total assembly length, number of contigs, and genome coverage.  
4. Record runtime and memory consumption for each assembler.  
5. Compare results to analyze trade-offs between assembly quality and computational efficiency.  

## Methodology
1. **Dataset Selection**  
   - Obtain Illumina sequencing datasets for bacterial genomes (e.g., *Escherichia coli*, *Bacillus subtilis*) from NCBI SRA.  
   - Choose datasets with varying read lengths and sequencing depths to assess robustness.  

2. **Assembly Process**  
   - Run each assembler using default parameters and document results.  
   - Perform additional runs with parameter tuning (e.g., k-mer size) to assess sensitivity.  

3. **Evaluation Metrics**  
   - **N50**: A measure of contiguity.  
   - **Total assembly length**: Compared to the known reference genome size.  
   - **Number of contigs**: Indicator of assembly fragmentation.  
   - **Genome coverage**: Proportion of the reference genome successfully reconstructed.  
   - **Runtime and memory usage**: Computational performance indicators.  

4. **Analysis**  
   - Summarize results using comparative tables and visualizations (e.g., bar charts).  
   - Identify strengths and weaknesses of each assembler.  
   - Discuss the suitability of each tool for different types of assembly tasks.  

## Tools and Datasets
- **Assemblers**: SPAdes, Velvet, SOAPdenovo  
- **Datasets**: Public bacterial Illumina datasets from NCBI SRA  
- **Evaluation Tools**: QUAST (Quality Assessment Tool for Genome Assemblies), Linux profiling utilities (time, memory)  
- **Programming Environment**: Linux command line; Python/R for result analysis and visualization  

## Expected Results
- A quantitative comparison of SPAdes, Velvet, and SOAPdenovo across multiple assembly metrics.  
- Identification of the strengths of each assembler (e.g., SPAdes for accuracy, Velvet for speed, SOAPdenovo for scalability).  
- Visualizations that clearly illustrate trade-offs in assembly quality and computational requirements.  
- A final report providing recommendations for assembler selection in microbial genome projects.  

## References
1. Bankevich A. et al. (2012). SPAdes: A New Genome Assembly Algorithm and Its Applications to Single-Cell Sequencing. *Journal of Computational Biology.*  
2. Zerbino D. R., Birney E. (2008). Velvet: Algorithms for de novo short read assembly using de Bruijn graphs. *Genome Research.*  
3. Luo R. et al. (2012). SOAPdenovo2: An empirically improved memory-efficient short-read de novo assembler. *GigaScience.*  
4. Gurevich A. et al. (2013). QUAST: Quality assessment tool for genome assemblies. *Bioinformatics.*  

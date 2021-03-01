# Interim data for the Oscheius genome sequencing at the Blaxter lab

:warning: **Warning: These sequences should not be considered final versions as more sequencing is underway and will be incorporated.**


## DNA extraction
Strains were received from Marie-Anne Felix. Robin Moll cultured the nematodes, extracted DNA. The long DNA was multiplexed to sequence two libraries per flowcell.

## Decontamination
HiFi reads were assembled with hifiasm and queried against a custom protein database with diamond blastx. The database was composed by the proteomes of *Caenorhabditis elegans*, *Bursaphelenchus okinawaensis*, *Escherichia coli str. K-12 substr. MG1655*, *Ochrobactrum pituitosum*, *Leucobacter triazinivorans* and *Brevundimonas diminuta*. HiFi reads were mapped against their corresponding assembly with minimap2. Blobtoolkit was used to discard reads that mapped to contigs that either had a GC content greater than 49% or were classified as bacteria according to hits against the proteomes database. The accepted reads were those not aligning to the assembly or mapping against nonbacterial classified contigs that had GC content lower than or equal to 49%.

Blobplots and Genomescope results can be found under the QC directory.

## Released assemblies
The filtered reads were assembled with Hifiasm, HiCanu, Flye and Redbean. The assembly with highest number of complete chromosomes or highest N50 was chosen as the best representative. 

## Authors

These sequences were generated thanks to the work of Pablo Gonzalez de la Rosa, Robin Moll, Manuela Kieninger, Sanger's DNA pipelines staff (Elizabeth Cook et al.), Marie-Anne Félix and Mark Blaxter.

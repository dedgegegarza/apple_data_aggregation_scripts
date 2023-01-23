# apple_data_aggregation_scripts
A list of scripts used to aggregate apple datasets from isolated sources. Includes two thesauri for aggregating accession names and marker names, respectively
These scripts can be downloaded and used directly in R or RStudio. The user will need raw ID input files (id.Raw files).

The Germplasm Identification Thesaurus (GIT) is used to aggregate multiple historical datasets where those datasets could link to individuals known by one or more
synonyms. For example, data for the 'Cripps Pink' cultivar could also be linked to the brand name Pink Lady. The SNP locus Identification Thesaurus (SIT) is used
to link aliases of the marker identifier for facilitating the aggregation of data linked to the same position in the genome.

The first id.Raw file can be used as input for the Germplasm Identification Thesaurus (GIT).
These id.Raw files are flat files (.csv) with the following fields:
1. id.Original - the original germplasm name or identifier of the received file
2. id.Plain - the original germplasm name or identifier (id.Original) of the received file without special characters/spaces, using only lower case letters and numbers
of the English alphabet
3. id.Raw - in many cases, the same as the id.Plain, but if ambiguous IDs are found, then this identifier is appended with extra passport information of the sample
4. id.Syn (if needed) - Extra passport information. Any available alias of the id.Original
5. syn.Plain (if needed) - Extra passport information. Similar to the id.Plain in format, but generated from the id.Syn
6. contrib - The contributor of the file
7. file_name - The name of the file
8. confidentiality - Whether the files content or private or public information
id.Raw files should be generated for all field measurement (phenotype) and marker (genotype) data

The second id.Raw file can be used as input for the SNP locus Indentification Thesaurus (SIT).
These sid.Raw (for SNP) files are also flat files (.csv) with the following fields:
1. sid.Raw - The original raw marker identifier linking the data to a specific position of the genome
2. sid.Syn - Extra passport information; other names or identifiers that the sid.Raw is known by
3. sid.Plain - plain text identifier of the sid.Raw or sid.Syn, using only lower case letters and numbers of the English alphabet and no special characters or
spaces.
4. 

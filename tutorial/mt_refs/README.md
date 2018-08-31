
The directory contains reference sequences from the West Indian Manatee (_Trichechus manatus_) downloaded from Genbank (accession number: AM904728).

 - `Trichechus_manatus.AM904728.fasta` - full mt genome
 - `Trichechus_manatus.AM904728.CDS.aa.fasta` - amino acid sequences of coding genes
 - `Trichechus_manatus.AM904728.CDS.nt.fasta` - nucleotide sequences of coding genes
 - `Trichechus_manatus.AM904728.COI.nt.fasta` - nucleotide sequence of the COI gene



FYI, these files were downloaded like so:
```bash
# declare basic variables
sp=Trichechus_manatus
acc=AM904728

# download the full mitochondrial genome using efetch and the accession number
rettype=fasta
wget -O - "http://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=nucleotide&id=${acc}&rettype=${rettype}&retmode=txt" \
> mt_refs/$sp.$acc.fasta

# download the CDS nucleotide sequences for the accession
rettype=fasta_cds_na
wget -O - "http://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=nucleotide&id=${acc}&rettype=${rettype}" \
> mt_refs/$sp.$acc.CDS.nt.fasta

# download the CDS amino acid sequences for the accession.
rettype=fasta_cds_aa
wget -O - "http://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=nucleotide&id=${acc}&rettype=${rettype}" \
> mt_refs/$sp.$acc.CDS.aa.fasta
```

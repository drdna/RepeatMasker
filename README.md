# RepeatMasker
## Masking of ALL operational repeats for accurate SNP calling
1. Place all genomes in a dedicated directory:
```bash
mkdir UnmaskedGenomes
cp *fasta UnmaskedGenomes
cd UnmaskedGenomes
```
2. Copy the [RMSA.pm](scripts/RMSA.pm) module into the PERL_MODULES directory and make it executable:
```bash
cp RMSA.pm perl_modules
chmod a+x RMSA.pm
```
3. Run the [RepeatMasker.pl](/scripts/RepeatMasker.pl) script:
```bash
for f in $(ls UnmaskedGenomes/*fasta); do perl RepeatMasker.pl $f; done
```

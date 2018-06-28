# ncbi_database_fetcher


ncbi_database_fetcher is a script that extract sequences from NCBI by term
```
usage : $0 <(-y term1 -y term2 | -y "term1 term2")> [(-n term1 -n term2 | -n "term1 term2")]

[-O <organism>] [-d (nucleotide|protein)] [-f <filename>] [-o <directory>]  [-v] [-h]

	-y list of key terms separated by space to be INCLUDED in sequences title
	-n list of key terms separated by space to be EXCLUDED in sequences title
	-O organism to filter
	-d database type, default nucleotide
	-o output directory (optional). By default the file is placed in cwd
	-f file name (optional). By default is the first term used as query
	-v version
	-h display usage message
```

### Example: 

If you want to download a database of plasmids from Archaea group use this command

```bash
./ncbi_database_fetcher.sh -y plasmid -n unnamed -n partial -O Archaea
```

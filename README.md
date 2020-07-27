# pgdb-retriever

 pgdb-retriever program takes a *Pseudomonas aeruginosa* locus tag (e.g PA14_73070) from [The Pseudomonas Genome Database](https://www.pseudomonas.com) 
 and it returns some of the information related to that locus tag. The retrieved information will be printed on screen in the json format.


## What you can retrieve:
* **locus tag**: The locus tag input by the user (`the gene` we are investigating)
* **gene**: The abreviated name of `the gene`
* **product name**: A more descriptive name of `the gene`
* **strain**: The strain of *P. aeruginosa* in which `the gene` is found
* **pseudocap**: List of PseudoCAP functions annotated to `the gene`
* **operon**: List of genes in the same operon as `the gene`
  


## Usage: 
```
python pgdb_retriever.py [-h] LOCUS_TAG
 positional arguments:
  LOCUS_TAG   the locus of interest

optional arguments:
  -h, --help  show this help message and exit
```

## Example:
 ```bash
 $ python pgdb_retriever.py PA14_73070                               
 {                                                                   
     "locus_tag": "PA14_73070",                                      
     "gene": "pyrQ",                                                 
     "product_name": "dihydroorotase",                               
     "strain": "Pseudomonas aeruginosa UCBPP-PA14",                       
     "pseudocap": [                                                  
         "Nucleotide biosynthesis and metabolism"                    
     ],                                                              
     "operon": [                                                     
         {                                                           
             "locus_tag": "PA14_73050",                              
             "gene_name": null,                                      
             "description": "GTP cyclohydrolase"                     
         },                                                          
         {                                                           
             "locus_tag": "PA14_73060",                              
             "gene_name": null,                                      
             "description": "hypothetical protein"                   
         },                                                          
         {                                                           
             "locus_tag": "PA14_73070",                              
             "gene_name": "pyrQ",                                    
             "description": "dihydroorotase"                         
         }                                                           
     ]                                                               
 }                                                                   
```

## If you use this tool
Ackonowledge The Pseudomnas Genome Database (PGDB) in any of your publications. 
>Nucleic Acids Res. (2016) doi: 10.1093/nar/gkv1227 (Database issue). Pubmed: [26578582](https://pubmed.ncbi.nlm.nih.gov/26578582/)

*I wrote this tool to retrieve data for my own projects and am not affiliated with The PGDB. To know more about my projects visit [my page](juliofdiaz.github.io)*

## Contact:
julio.diaz@zoo.ox.ac.uk

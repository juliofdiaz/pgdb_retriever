


 pgdb-retriever program takes a *Pseudomonas aeruginosa* locus tag (e.g PA14_73070) from [The Pseudomonas Genome Database](https://www.pseudomonas.com) 
 and it returns some of the information related to that locus tag. The retrieved information will be printed on screen in the json format.


## What you can retrieve:
* **locus tag**: The locus tag input by the user
* **gene**: The abreviated name of the gene
* **product name**: A more descriptive name of the gene
* **strain**: The 
* **pseudocap**: relative paths to files. The only mandatory option.
  It could be a path `"index.js"`, a [pattern] `"dist/app-*.js"`
  or an array `["index.js", "dist/app-*.js", "!dist/app-exclude.js"]`.
* **operon**: relative paths to files. The only mandatory option.
  It could be a path `"index.js"`, a [pattern] `"dist/app-*.js"`
  or an array `["index.js", "dist/app-*.js", "!dist/app-exclude.js"]`.
  


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


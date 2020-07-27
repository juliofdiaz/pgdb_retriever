


 This program takes a *Pseudomonas aeruginosa* locus tag (e.g PA14_73070) from [The Pseudomonas Genome Database](https://www.pseudomonas.com) 
 and it returns some of the information related to that locus tag. The retrieved information will be printed on screen in the json format.

Usage: 
```
python pgdb_retriever.py [-h] LOCUS_TAG
 positional arguments:
  LOCUS_TAG   the locus of interest

optional arguments:
  -h, --help  show this help message and exit
```

 Example:
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

@author: juliofdiaz.github.io

positional arguments:
  LOCUS_TAG   the locus of interest

optional arguments:
  -h, --help  show this help message and exit

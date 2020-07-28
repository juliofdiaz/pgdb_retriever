# pgdb-retriever

pgdb-retriever searches the  [The Pseudomonas Genome Database](https://www.pseudomonas.com) for information related to a user-input locus tag (e.g PA14_73070). I wrote this code because I wanted to obtain the PseudoCAP functional annotation for more than a few loci. The retrieved information will be printed on screen in the json format.

## What you can retrieve:
* **locus tag**: The locus tag input by the user (`the gene` we are investigating)
* **gene**: The abreviated name of `the gene`
* **product name**: A more descriptive name of `the gene`
* **strain**: The strain of *P. aeruginosa* in which `the gene` is found
* **pseudocap**: List of PseudoCAP functions annotated to `the gene`
* **operon**: List of genes in the same operon as `the gene`
  
## Install:

Ypu can simple download the [pgdb_retriever.py](https://raw.githubusercontent.com/juliofdiaz/pgdb_retriever/master/pgdb_retriever.py) or clone this repository:

```bash
git clone https://github.com/juliofdiaz/pgdb_retriever.git
```

You will need these Python libraries:
* [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#installing-beautiful-soup): `pip install beautifulsoup4` OR `conda install -c anaconda beautifulsoup4`
* [Requests](https://requests.readthedocs.io/en/master/user/install/): `pipenv install requests` OR `conda install -c anaconda requests`

I have tried pgdb-retriever with Python 3.5+

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
If you use the data you retrieved with this tool in any of your publications, please ackonowledge The Pseudomnas Genome Database (PGDB).
>Nucleic Acids Res. (2016) doi: 10.1093/nar/gkv1227 (Database issue). Pubmed: [26578582](https://pubmed.ncbi.nlm.nih.gov/26578582/)

*I wrote this tool to get data for my own projects and am not affiliated with The PGDB. If you use this little tool, please take a moment to acknowledge you are a rockstar :star2:. To know more about my projects visit [my page](juliofdiaz.github.io)*

## Contact:
julio.diaz@zoo.ox.ac.uk

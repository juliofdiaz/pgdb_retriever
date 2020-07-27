# pgdb_retriever
Retrieve information of a specific locus from Pseudomonas Genome Database


usage: pgdb_retriever.py [-h] LOCUS_TAG

#######################################################################
#                                                                     #
# This program takes a locus tag from The Pseudomonas Genome Database #
# and it returns some of the information related to that locus tag.   #
# The info will be printed to screen in the json format.              #
#                                                                     #
# Example:                                                            #
# $ python pgdb_retriever.py PA14_73070                               #
# {                                                                   #
#     "locus_tag": "PA14_73070",                                      #
#     "gene": "pyrQ",                                                 #
#     "product_name": "dihydroorotase",                               #
#     "strain": "Pseudomonas aeruginosa UCBPP-PA14",                  #
#     "pseudocap": [                                                  #
#         "Nucleotide biosynthesis and metabolism"                    #
#     ],                                                              #
#     "operon": [                                                     #
#         {                                                           #
#             "locus_tag": "PA14_73050",                              #
#             "gene_name": null,                                      #
#             "description": "GTP cyclohydrolase"                     #
#         },                                                          #
#         {                                                           #
#             "locus_tag": "PA14_73060",                              #
#             "gene_name": null,                                      #
#             "description": "hypothetical protein"                   #
#         },                                                          #
#         {                                                           #
#             "locus_tag": "PA14_73070",                              #
#             "gene_name": "pyrQ",                                    #
#             "description": "dihydroorotase"                         #
#         }                                                           #
#     ]                                                               #
# }                                                                   #
#                                                                     #
#                                                                     #
#######################################################################

@author: juliofdiaz.github.io

positional arguments:
  LOCUS_TAG   the locus of interest

optional arguments:
  -h, --help  show this help message and exit

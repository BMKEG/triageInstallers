
Requirements:
Software:
- swfTools (http://www.swftools.org/). Installation guides: (http://wiki.swftools.org/wiki/Installation)

- MySql v 5.1

Server:
  - Own a port number to process http requests from client web browsers
  - Need to send http requests to http://eutils.ncbi.nlm.nih.gov (the PubMed citations index)
  - Needs to login (using a given username) to MySql and have privileges to create (and destroy) databases

Commands:

setSwfToolsBinDirectory DIRECTORY

buildTriageDatabase -db DBNAME -l LOGIN -p PASSWORD

editArticleCorpus -name NAME -desc DESC -owner OWNER -db DBNAME -l LOGIN -p PASSWORD

editTriageCorpus -name NAME -desc DESC -owner OWNER -db DBNAME -l LOGIN -p PASSWORD

addPmidEncodedPdfsToCorpus -pdfs PDFS-DIR-OR-FILE -corpus CORPUS -db DBNAME -l LOGIN -p PASSWORD [-rules FILE]

buildTriageCorpusFromPmidList -triageCorpus NAME -targetCorpus NAME -pmidCodes CODE-FILE -db DBNAME -l LOGIN -p PASSWORD

triageDocumentsClassifier triageCorpus -triageCorpus NAME-targetCorpus NAME -modelDir DIR -db DBNAME -l LOGIN -p PASSWORD [-train -predict]

triageServer -db DBNAME -l LOGIN -p PASSWORD


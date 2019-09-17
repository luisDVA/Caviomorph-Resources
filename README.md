## Supplementary materials README guide 
# Patterns in research and data-sharing for the study of form and function in caviomorph rodents

Data description and general guide for working with the files uploaded to the repository. 
Supplementary materials files are organized in the following three folders:


📂  master_lists 

Comma-separated text files with aggregate data from all studies, the reference taxonomy used throughout the analyses, and the data used to standardize and geocode the collections housing caviomorph specimens. These files are used by the RMarkdown reporting scripts. 

| File                       | Description                                                                                       |
|----------------------------|---------------------------------------------------------------------------------------------------|
| asm-species-2018-10-02.csv | Reference taxonomy, downloaded from Mammaldiversity.org (downloaded November 2018)                |
| master-accessions.csv      | DNA sequence identifiers                                                                          |
| master-diet.csv            | Feeding strategies/diets                                                                          |
| master-habitats.csv        | Habitat preferences                                                                               |
| master-habits.csv          | Substrate use strategies/habits                                                                   |
| master-morph.csv           | Morphology trait values                                                                           |
| master-specimens.csv       | Specimens examined with standardized and geocoded collection data                                 |
| museums.csv                | Standardized collection names (see main text for sources)                                         |
| museum_locations.csv       | Collection locations, obtained through the Opencage geocoding service (https://opencagedata.com/) |


📂  relational_data

Comma-separated text files containing all the redigitized data available in the 36 studies reviewed. Two common variables in the files can be used to establish relationships between them; the `sp` column contains the study taxa (observational units) and the `study` column refers to the source of the data. Redigitized data is also available as single Open XML workbook (`relational_all.xlsx`) with separate worksheets for each file. 



Each file name (shown below without the file extension) is labeled with the following suffixes to identify its content: 

| File suffix    | Description                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| *_accessions   | Identifiers for DNA sequences                                                           |
| *_traits_eco   | Ecological trait values                                                                 |
| *_traits_morph | Morphology trait values                                                                 |
| *_specimens    | Specimens examined                                                                      |
| *_linear       | Names and descriptions of the linear traits and compound indices examined or calculated |
| *_landmarks    | Description of landmark configurations used in geometric morphometrics analyses         |

📂  scripts

RMarkdown scripts to query the data for particular species and produce customized reports, which can be rendered as .pdf, .html, or .doc files. In both files, changing the of `focalSp` object defines the input for user-defined scientific name queries.

The code relies on the `here` package and will run best if all files and folders are downloaded and set up in the following directory structure:

├ ─ ─ overall project workspace  
│   ├── master_lists  
│   ├── relational_data  
│   └── scripts  

| File | Description |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| report-morphology.Rmd | Produces a report focusing on morphological trait values and the descriptions of the available traits. |
| report-overview.Rmd | Produces an overall summary of the morphological and ecological trait data, as well as specimen holdings and DNA accession IDs used across all the studies reviewed. |




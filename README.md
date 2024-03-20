# Pseudonymize - Data Privacy Enhancement with Hashing
This script aims to enhance data privacy by identifying and hashing specific elements using MD5 + SALT. The recognized elements include emails, IBANs, phone numbers, and unidentified individuals. 

# Named Entity Recognition (NER) Integration
The script utilizes Spacy's Named Entity Recognition (NER) to identify individuals (PER). If these individuals are not listed as known US, UK, or DE politicians, their information is also hashed with MD5 + SALT. Politicians' data remains unchanged. The list of politicians comes form the [everypolitician-names](https://github.com/everypolitician/everypolitician-names) project. The scrip filters out street names based on a regex and locations detected by Spacy. All major country names and cities are excluded, they are provided by [countries-states-cities-database](https://github.com/dr5hn/countries-states-cities-database/tree/master). 

# Social Media Usernames Integration
Extend the NER to include social media usernames, as shown in the script. There social media handels starting with "@" are extracted and the added to the Spacy pipeline.

# Room for Improvement
* AI Limitations: The Spacy NER, being AI, may not be flawless. Continuous improvement is possible.
* Regex Optimization: Regex expressions can be further optimized for different formats.
* Entity Linker Consideration: While an ideal approach involves replacing the politician list with an Entity Linker to Wikidata
* Train own Model to detect the different entities
* MD5 could be replaced by a more secure option

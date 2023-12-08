# Pseudonymize - Data Privacy Enhancement with Hashing
This script aims to enhance data privacy by identifying and hashing specific elements using MD5. The recognized elements include emails, IBANs, phone numbers, and unidentified individuals.

# Named Entity Recognition (NER) Integration
The script utilizes Spacy's Named Entity Recognition (NER) to identify individuals (PER). If these individuals are not listed as known US, UK, or DE politicians, their information is also hashed with MD5. Politicians' data remains unchanged. The list of politicians comes form the [everypolitician-names](https://github.com/everypolitician/everypolitician-names) project.

# Social Media Usernames Integration
Extend the NER to include social media usernames, as hinted in the script. This can be run parallel to the existing list of politicians, providing a comprehensive approach.

# Room for Improvement
* AI Limitations: The Spacy NER, being AI, may not be flawless. Continuous improvement is possible.
* Regex Optimization: Regex expressions can be further optimized for different formats.
* Entity Linker Consideration: While an ideal approach involves replacing the politician list with an Entity Linker to Wikidata

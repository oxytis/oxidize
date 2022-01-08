# Oxidize - tactical version

Discover PII sensitive data. Find personally identifiable information in your environment such as financial. Quickly determine exposure after a breach. Most common elements Dates of Birth, Social Security Numbers, Credit Card Numbers, and other Tax ID Numbers are searched for as these are most likely to be associated to an individual. Other quasi identifying data will not be checked as it is not meaningful or useful unless associated. Does not satisfy data breach reporting requirements, for that use Oxytis "oxidize" service.

Useful during network assessments by red teams who are looking for the "loot" in a post-exploitation scenario. Add oxidize to your toolkit!

Tactical version written in Go is available in 64-bit versions for both Windows and Linux for finding data impacting U.S. residents.

Find the most common data elements SSN, Tax IDs, CCN, and DOB in PDF, DOC|DOCX, XLS|XLSX, EML, Plain|Text|CSV, and files in ZIP archives!.

Additional dependencies -> "apt install poppler-utils wv unrtf tidy".

adding -loot option saves the data to a zip file.

<b>Usage:</b> ./oxidize --path ../data/testdata --loot

Adding --powertrain option outputs "oxidize.txt" file, upload to powertrain with config file for a report, US only.

<b>Usage:</b> ./oxidize --path ../data/testdata --loot --powertrain"


Adding --remote option copies l00t to a remote host via ssh

<b>Usage:</b> ./oxidize --path ../data/testdata --loot --powertrain --remote="user:pass:host"

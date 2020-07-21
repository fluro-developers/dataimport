
# Data Import 
Requires NodeJS 

# Installation

```
git clone git@github.com:fluro-developers/dataimport.git
```
```
cd dataimport
```
```
npm install

```


# Adding your files
Add any CSV documents you want to import into the /files folder, then run the script

# Run
```
node index.js
```



# Data Mapping
Adjust Column Names for your CSVs by editing the index.js document before running the script.

### How it works
This script will first prompt you to login, then ask you to select:
- An account
- A default realm
- The file you wish to import
- The kind of import (3 options, Attendance checkins, Headcount Numbers or Contact Notes)

Once you have started the import, it will sequentially iterate through each of the rows and run a check to see if the row has already been imported in to your account,
if it has not been imported yet it will then create it and continue. This means it is safe to import the same document multiple times without creating duplicate records.
If you see your terminal printing 404 connection issues, this is standard and actually a good thing, it's telling you that the document does not exist and it will try and create it
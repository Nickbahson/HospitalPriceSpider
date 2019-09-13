#File contains steps and choices made in each

##Stage 1: Convert csv to json
##Stage 2
##Stage 3
##Stage 4

#Stage 1
I needed to atleast present some data to a browser, so I opted for
express js, to help me convert csv data to json, I used the library
csvtojson `https://www.npmjs.com/package/csvtojson` which is well 
maintained, instead of writing my own read file functions which would
take alot of the project time, not to mention the bugs that comes with
such. I trust csvtojson is a good choice for this mission.

###Project setup
Added files/folders
+ package.json 
+ index.js // our express server file
+ ./services/csvToJson.js // module that converts csv to json given file path

### Preview the project
run `yarn install` or `npm install` to download and install express and
 csvtojson and their dependencies.
 
 In the project root dir, run node index.js to start express server,
 You will get an output also to the console of the data in file
 McLean_Hospital.csv, also access the same json data via the port your
 app is working on, in my case http://localhost:3007/api/test/.
 The fields data are unmatched and other files data can be retrived via
 the same way by editing index.js on line 19
 
 ##Stage 2
 Clone this repo, cd into that directory, run `yarn install` or `npm install`,
 and after that run node index.js to start server on `http://localhost:3007/`.
 Go to `http://localhost:3007/api/csv-files` to access all csv files in
 our folder.
 Go to `http://localhost:3007/api/csvdata/availableFileName.csv` eg
 `http://localhost:3007/api/csvdata/hospital_Baton-Rouge-General-Medical-Center.csv`
 to view the content to each file in json.
 You many copy each of the names displayed on the list on `http://localhost:3007
 /api/csv-files` and add to `http://localhost:3007/api/csvdata/TheCopiedFileNamePlus.Extension`
 to test.
 
 ##Stage 3
 
 ##Stage 4 
 So far, I have added scripts to convert csv to json, and spreadsheet to json.
 To test, clone this repo and cd to the dir, run `yarn install` or `npm install` to install
 the required libraries.
 Then run `node index.js` to start the local server at port `http://localhost:3007`.
 The endpoint are(with the post current)
 
 1. `http://localhost:3007/api/data/local-spreed-sheets`
 Lists all spreadsheets available in the local folder
 
 2.`http://localhost:3007/api/data/local-xlsl-file/{filename.xlsx}`
 Displays the content of the spreadsheet in json format, remember a valid
 name that is available in the local folder, for ideas see 
 `http://localhost:3007/api/data/local-spreed-sheets`
 
 3. To avoid repetition, please refer to stage2 and 1 to know the other api
 endpoint and what the return.
 
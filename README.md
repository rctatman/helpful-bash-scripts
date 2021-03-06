## Helpful Bash Scripts

A collection of helpful Bash utility scripts so I can remember them instead of immediately forgetting & having to Google them the next time I need them. You might find them helpful too.

Important note: you *never* put spaces around the = when it's used for variable assignment.

|What it does|Command|
|---|---|
|Concatinates .json files| jq -s 'reduce .[] as $item ({}; . * $item)' *.json > ouputFile.json|
|Print just the wordcount of .txt files|wc -w *.txt|
|Save a list of all files in your current directory|ls>list-of-files.txt|
|Check the character encoding of a file|file -i file-name.txt|
|Add file directory info to file names and move to current directory|for i in */*.txt.clean;do new=$(echo $i \| sed -e 's/\//_/g'); mv ${i} ${new}; done|

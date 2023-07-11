To find a PDF file with "hadoop" in the title or inside using PowerShell, you can use the following command:


Get-ChildItem -Path C:\path\to\search -Recurse -Include *.pdf | Where-Object { $_.Name -match 'hadoop' -or (Get-Content $_.FullName -Raw) -match 'hadoop' }


- Here's what each part of the command does:

Get-ChildItem: This cmdlet gets a list of files and directories in the specified path.
-Path: This specifies the path to search for PDF files.
-Recurse: This tells PowerShell to search recursively through all subdirectories.
-Include: This specifies that we only want to search for PDF files.
Where-Object: This filters the results to only include files that meet certain criteria.
{ $_.Name -match 'hadoop' -or (Get-Content $_.FullName -Raw) -match 'hadoop' }: This is the filter criteria. It looks for files where the name or the contents match the string "hadoop".
Note that you'll need to replace C:\path\to\search with the actual path you want to search.






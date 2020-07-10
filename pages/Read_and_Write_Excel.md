---
autogenerated: true
title: Read and Write Excel
breadcrumb: Read and Write Excel
layout: page
author: test author
categories: 
description: test description
---

plugins/Read\_and\_Write\_Excel-1.1.2

Authors: Anthony Sinadinos and Brenden Kromhout

Description : By default, this plugin extracts data from the Results Table and adds it to a sheet-tab "A" in an .xlsx Excel file on the user's desktop. The plugin will create a file named "Rename me after writing is done" on the desktop if none-exists already, and will update this file if it has already been created. Data is added to the latest sheet (created as "A" if the file is new) or to a user specified sheet using a passed argument (see below). Within the latest sheet, data will be added adjacent to previous data, unless an argument is passed to stack results data into existing columns of the spreadsheet. Results Table column headers are added automatically. A row count is added by default but the user can choose to deny this with a passed argument.

This plugin can be called from a macro using: run("Read and Write Excel"); and it works very well with batching. A major change for v1.1.0, is that, if called slightly differently (see below), the plugin is now much better at handling large data sets and/or excel files that become large over time.

The title of the most recent open image will now be added as a label for exported results data by default, instead of the first open image. An argument function can also be used to overwrite this, so that the user may provide their own title for each export: run("Read and Write Excel", "dataset\_label=This\_is\_my\_new\_title"); Please note, the provided title should not contain spaces between words.

OPTIONAL ARGUMENTS will be parsed from the second argument string as follows.

"no\_count\_column" Prevents the plugin from adding a "Count" column automatically.

"stack\_results" Causes the plugin to export results data underneath pre-existing data (instead of adjacent to it). NOTE: The dataset label for the now stacked data will be that determined for the most recent import.

"file=" The path to the excel file to use (uses the default desktop file otherwise) Example "file=\[/Users/antinos/Desktop/My\_file.xlsx\]" will create and/or append the specified file.

"sheet=" Which sheet in the excel file to put the results in. Example "sheet=banana" will create and/or append a sheet named 'banana'.

"dataset\_label=" The label to write in the cell above the data in the excel file. Example "dataset\_label=My\_new\_results\_data\_label" will use the specified title. Strings and numbers can still be fed to the custom title modifier from a loop but avoid introducing spaces e.g "dataset\_label=Table\_" + i

Join arguments as follows: run("Read and Write Excel", "no\_count\_column file=\[/Users/antinos/Documents/My\_cool\_file.xlsx\] sheet=Custom\_name\_here dataset\_label=Table\_" As you can see, spaces are important to delimit arguments, hence us avoiding them within custom fields.

"file\_mode=" This requires a slightly different way of calling the plugin but is very useful for expected large datasets. There are three options. "file\_mode=read\_and\_open" Will just open an excel file (the one you specify with file=)...make sure you do write\_and\_close when you're done or you'll have problems. "file\_mode=write\_and\_close" Will just write everything you've queued with queue\_write, then close the excel file. "file\_mode=queue\_write" Will queue something to be written to the excel file you've opened previously with read\_and\_open

see https://github.com/bkromhout/Read_and_Write_Excel_Modified for examples.

I am aware that another Excel\_Writer plugin exists but it did not work for me very well (hence me creating this). I did not consult their source code but did find out about Apache POI(\*) from them.

Since Brenden modified the plugin, the code is now a lot neater. Feel free to consult it as per your needs.

(\*)This plugin uses the Apache POI api, which is distributed under the terms of the Apache Licence (available from https://poi.apache.org/legal.html). I believe this software to be free and open source.

Link: YouTube tutorial v1.0.1 (https://www.youtube.com/watch?v=79rzUae-7N8) New tutorial for v1.1.0 (https://youtube.com/watch?v=dLkoB25MTIY)
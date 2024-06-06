---
publish: true
title: Import your Audible Library to Goodreads
date: 2020-02-06
slug: import-your-audible-library-to-goodreads
author: Andrew Lovett-Barron
image: 9f2ee1b9cfb7dc43a72534f0f3faa380b74c9cb3-5955x3975.jpg
description: ""
tags:
  - technical
  - audible
  - howto
public: true
modified: 2024-06-07T01:30
---

I wrote a rudimentary python script to bulk import your Audible library to Goodreads. I’ll caveat with a statement: this is still pretty manual, but it automates the parts that are most time consuming. Overall, it shouldn’t take more than 5min to get your whole audible library into Goodreads. Then maybe just re-run the process every few months.

[You can view the script here](https://gist.github.com/readywater/b71c11428a151654474cdb673756319e)

## Get Your Audible Data

It procedurally builds off of another script that [exports your audible library](https://www.themodernnomad.com/audible-statistics-extractor/) , which is required to get it working. To run this script, [visit your audible library](https://www.audible.com/lib?purchaseDateFilter=all&programFilter=all&sortBy=PURCHASE_DATE.dsc&pageSize=50) and run the script on each page by hitting command-option J to open your console (in Chrome and most other browsers), and run this script (which is just a minified version of the [one linked above](https://www.static-18.themodernnomad.com/wp-content/uploads/2019/01/Audible-ScreenScraperJanuary2019.txt))

[Link to script](https://gist.githubusercontent.com/readywater/b71c11428a151654474cdb673756319e/raw/02f4e875aa1e55986c6e08a9dffd818bd7d92163/minified_audible_table_generator.js)

This will grab your library and turn the page into an html table. You can then easily select all on this table and paste it into google sheets or excel. Make sure to remove the repeated header data, but keep the top line.

You need to do this **for each page** of the library, so if you have 50+ books, simply go through each. Save the output; you can keep the file in an excel format or export to CSV.

## Convert the Data into a Goodreads Format

From here, you’ll want to run [the python script](https://gist.github.com/readywater/b71c11428a151654474cdb673756319e). Save the file to whatever directly you’ve stored your audible spreadsheet and open your terminal. On Mac, do this by typing command space and writing terminal in the spotlight search.

Before running the script, you’ll want to change two things. Open then python script and change line 17: df = pd.read_excel(r’/path/to/the/saved/excel.xlsx’) to the path to your file and line 35: df.to_csv(r’/path/to/export/audible-goodreads-import.csv’) to your export CSV format.

Then simply run py audible-goodreads-import.py in terminal, and you should get a file output with the CSV.

From there, simply [go to your goodread account’s import page](https://www.goodreads.com/review/import) and follow the import instructions.

It will import and update current read status, ratings, correct ISBN, and add it to an “audible” bookshelf.

## Next steps

Hopefully this serves to compliment other solutions out there, or as a starting point for someone who wants to put together a better solution for non-technical folk.

If you encounter bugs or improve the script somehow, please leave a comment below or in the [GitHub gist](https://gist.github.com/readywater/b71c11428a151654474cdb673756319e). If this works out for folk, I might put together something a bit more automated and a bit more user friendly eventually, but for a quick script thrown together while watching [Next in Fashion](https://www.netflix.com/dk-en/title/81026300), this works nicely.

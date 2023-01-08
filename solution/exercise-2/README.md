# Learn about command line, piping

This exercise contains more advanced shell workflow, including grep
and piping.  You can get a quick overview of piping at
[Unix/Linux - Pipes and Filters](https://www.tutorialspoint.com/unix/unix-pipes-filters.htm). 

Use the data (fake_news_sites.csv) provided in the data folder.  Use
command line to answer the questions below.  Learn about the command
using either **man**, or just google search for the documentation.
The data contains fact-checking results -- either correct, mostly
correct, or fake, for three news sites --- 1, 2, 3.

1. Compress the data.

   Use either *gzip* or *bzip2*.  Note: you have either to navigate to
   the right folder first, or alternatively submit the file name with
   folder name.

```bash
bzip2 data/fake_news_sites.csv
# you may want to see the file name and size:
ls -l data
```

2. View a first few lines of the data to understand it's structure.  

```bash
bzcat data/fake_news_sites.csv.bz2 | head
```

3. How many factually correct news are there?

   hint: use *zcat* or *bzcat* to display the text, use *grep* to search
   for a relevant pattern, use *wc* to count the resulting lines
   
```bash
bzcat data/fake_news_sites.csv.bz2 | grep "factually correct" | wc
```

   Note: `wc` returns three numbers: number of lines, words, and
   characters.  If you are only interested in number of lines, you may
   use `wc -l`.

4. How many mostly correct news are there?

```bash
bzcat data/fake_news_sites.csv.bz2 | grep "mostly correct" | wc
```

5. How many fake news are there?

```bash
bzcat data/fake_news_sites.csv.bz2 | grep "fake news" | wc
```

6. How many different types of news classifications are there?

   Hint: add up the types you see (you may use *head* to inspect the
   file).  Do you get the total number of observations?

   Find the total number of lines:
```bash
bzcat data/fake_news_sites.csv.bz2 | wc
```
   Do factually correct, mostly correct, and fake news counts sum to
   this number?  They have to sum to this number - 1 because `wc` also
   counts the header line with column names.
   
   

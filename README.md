# DB Class Exercises
This includes materials, exercises and solutions used in the [DBclass](https://class2go.stanford.edu/db/Winter2013) offered by Stanford.


## 2. SQL Exercises
This includes exercises for sql in the classes.
The first line in all examples is used by the `dbext` vim plugin to correctly connect to the right database.

### How to Run
Option 1, open a sqlite3 console with `sqlite3` and copy and paste the SQL in the console.
          then load the data bases using `attach "movie_rating.db" as db1`;

Option 2, uses the [`dbext`][dbext-link] vim plugin to communicate with the sqlite3 database. Select the sql in visual mode, execute `:DBExecRangeSQL` or press `<leader>se`.

## 3. XML Exercises
This includes exercises for xml .

The `utils/bin` folder contains script to run xquery or xslt easier.

The `utils/xquery-helper.vim` contains an util funciton I used to make xquery easier to run inside vim.

## Install Xpath/XSLT Implementations
First, install the xpath/xslt implementation on unix system - [saxon](http://www.saxonica.com/).

On Mac:

    brew install saxon

Others, follow the instruction on the official site.

### How to Run Xpath/Xquery
Use the bin file `utils/bin/xquery` in this repo. It is a simple wrapper around `saxon` to make queries easier to type. 

**Important**: Each xpath file should only contain one `return` clause, so if you run the xquery manually, you need to **comment out other clauses** to make it run.

    xquery <xpath file>

If you are using `vim` you could use the function I write in vim to run the pieces of code one by one. Just select the code you need to run into a visual block, and press`<leader>xe` to run them.

More detailed usage: checkout the document on the [official site](http://www.saxonica.com/documentation/using-xsl/commandline.xml) for more details.

### How to Run XSLT
Use the bin file `utils/bin/xslt` in this repo. It is a simple wrapper around `saxon` to make queries easier to type. 

    xslt -xsl:<xslt file> <original xml>

For example

    xslt -xsl:core-q1.xsl courses.xml

More detailed usage: checkout the document on the [official site](http://www.saxonica.com/documentation/using-xquery/commandline.xml) for more details.

## 4. Constains and Triggers / 5. Views
Same as 3.SQL

[dbext-link]: https://github.com/vim-scripts/dbext.vim

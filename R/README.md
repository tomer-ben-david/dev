# Parsing Lines and Text Files

## Filter lines in text file

```R
lines = readLines("mylog.log")
lines[c(grep(pattern = "Controller", x = lines))]
```

## Regular expressions with grouping

```R
install.packages("stringr") # One time

library("stringr")
s = c("(sometext :: 0.1231313213)", "(moretext :: 0.111222)")
str_match(s, "\\((.*?) :: (0\\.[0-9]+)\\)")
```

## Read table like text file

could be separated by spaces but looks like a table for example

```
12312312312  1  2  somename
12312312312  4  1  someothername
```

```R
dfrm <- read.table("somefile.txt")
```

# Substring or match something in string of lines

```R
http://stackoverflow.com/questions/17215789/extract-a-substring-in-r-according-to-a-pattern
http://stackoverflow.com/questions/20075135/multiple-separators-for-the-same-file-input-r
```

# Plotting

## Line chart

Remember you need to `transpose` you need a vector of numbers not a column of numbers so assuming we have list of columns or something we are going to use `t()` to transform it.

```R
plot(t(mydata["COLUMN1"]), t(mydata["COLUMN2"]))
```


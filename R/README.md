# Parsing Lines and Text Files

## Filter lines in text file

```R
lines = readLines("mylog.log")
lines[c(grep(pattern = "Controller", x = lines))]
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


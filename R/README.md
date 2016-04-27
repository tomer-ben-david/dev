# Parsing Lines and Text Files

## Filter lines in text file

```R
lines = readLines("mylog.log")
lines[c(grep(pattern = "Controller", x = lines))]
```

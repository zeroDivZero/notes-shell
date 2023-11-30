# `diff`

Finds differences in files.

```sh
diff file1.txt file2.txt
```

Shows instructions like `5c5,6` (line 5 in first file changed to line 5 and 6 in second), `11a13,15`, `3d2`, etc. to make two files match.

```sh
diff -c file1.txt file2.txt
```

Shows in **context** mode, which provides more info about the differences. Use `-u` for **unified** mode, which is like context mode but more concise because it doesn't show redundant info.

## Conditional Complexity
Conditional complexity is a code smell that can be detected by looking at your conditional checks, such as if statements. If they're extremely long or have the potential to become long in the near future, then you've found the smell.

In our example, we have an if statement that checks a file extension. We use it to avoid animated files that aren't images. Since we may come across more file extensions in the future that we want to ignore, or potentially brand new file extensions, a better solution would be putting all the extensions in a list rather than a long one-line.

```{python}
 if fextension != ".gif" and fextension != ".mp4" and fextension != ".mov" and fextension != ".flv" and fextension != ".gifv":
```



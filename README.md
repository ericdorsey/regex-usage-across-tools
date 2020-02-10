### Links
* https://www.johndcook.com/blog/powershell_perl_regex/

### Find Matching Values Given a Regex Pattern

#### PowerShell
```powershell
PS C:\> ([regex]::matches("foo bar Baz", "\w+", "IgnoreCase") | ForEach { $_.value})
foo
bar
Baz
```

#### Python
```python
In [140]: import re
In [141]: re.findall(r"\w+", "foo bar Baz", re.IGNORECASE)
Out[141]: ['foo', 'bar', 'Baz']
```

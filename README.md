### Links
* https://www.johndcook.com/blog/powershell_perl_regex/
* https://stackoverflow.com/questions/43421755/powershell-regex-match-only-matching-once/43421819#43421819


### Find Matching Values Given a Regex Pattern

#### PowerShell
```powershell
PS C:\> ([regex]::matches("foo bar Baz", "\w+", "IgnoreCase") | ForEach { $_.value})
foo
bar
Baz
```

```powershell
PS C:\> ("foo bar Baz" | Select-String -AllMatches "\w+").Matches.Value
foo
bar
Baz

PS C:\> ("foo bar Baz" | Select-String -AllMatches "\w+").Matches.Count
3
```

#### Python
```python
In [140]: import re
In [141]: re.findall(r"\w+", "foo bar Baz", re.IGNORECASE)
Out[141]: ['foo', 'bar', 'Baz']
```

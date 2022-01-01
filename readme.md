# SICP3 Translation

By Deepl and a simple python script

```python
from clipboard import copy, paste

def remove_enter(s: str) -> str:
    s_new = ""
    for i, c in enumerate(s):
        if c == "\n":
            if s[i - 1] == ".":
                s_new += c
            # fix scheme code
            elif s[i + 1] == "(":
                s_new += c
            elif s[i - 1] == ")":
                s_new += "\n"
            else:
                s_new += " "

        else:
            s_new += c
    return s_new + "\n\n"

copy(remove_enter(paste()))
```

Work flow:

1. open pdf
2. copy an article
3. run script to fix format
4. paste to a docx
5. deepl translate it

Use website, you can only translate 5k characters at a time. But you can translate 100k characters at a time by docx.

---

TODO:

- fix some code translate by deepl.
- adjust the format.

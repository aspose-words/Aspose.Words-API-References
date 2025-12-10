---
title: FindReplaceOptions.legacy_mode property
linktitle: legacy_mode property
articleTitle: legacy_mode property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.legacy_mode property. Gets or sets a boolean value indicating that old find/replace algorithm is used."
type: docs
weight: 140
url: /python-net/aspose.words.replacing/findreplaceoptions/legacy_mode/
---

## FindReplaceOptions.legacy_mode property

Gets or sets a boolean value indicating that old find/replace algorithm is used.


```python
@property
def legacy_mode(self) -> bool:
    ...

@legacy_mode.setter
def legacy_mode(self, value: bool):
    ...

```

### Remarks

Use this flag if you need exactly the same behavior as before advanced find/replace feature was introduced.
Note that old algorithm does not support advanced features such as replace with breaks, apply formatting and so on.


### Examples

Shows how to recognize and use substitutions within replacement patterns.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Jason gave money to Paul.')
regex = '([A-z]+) gave money to ([A-z]+)'
options = aw.replacing.FindReplaceOptions()
options.use_substitutions = True
# Using legacy mode does not support many advanced features, so we need to set it to 'false'.
options.legacy_mode = False
doc.range.replace_regex(pattern=regex, replacement='$2 took money from $1', options=options)
self.assertEqual(doc.get_text(), 'Paul took money from Jason.\x0c')
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)


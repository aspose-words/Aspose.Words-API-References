---
title: FindReplaceOptions.match_case property
linktitle: match_case property
articleTitle: match_case property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.match_case property. True indicates case-sensitive comparison, false indicates case-insensitive comparison."
type: docs
weight: 140
url: /python-net/aspose.words.replacing/findreplaceoptions/match_case/
---

## FindReplaceOptions.match_case property

True indicates case-sensitive comparison, false indicates case-insensitive comparison.


```python
@property
def match_case(self) -> bool:
    ...

@match_case.setter
def match_case(self, value: bool):
    ...

```

### Examples

Shows how to toggle case sensitivity when performing a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Ruby bought a ruby necklace.")

# We can use a "FindReplaceOptions" object to modify the find-and-replace process.
options = aw.replacing.FindReplaceOptions()

# Set the "match_case" flag to "True" to apply case sensitivity while finding strings to replace.
# Set the "match_case" flag to "False" to ignore character case while searching for text to replace.
options.match_case = match_case

doc.range.replace("Ruby", "Jade", options)

self.assertEqual(
    "Jade bought a ruby necklace." if match_case else "Jade bought a Jade necklace.",
    doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)


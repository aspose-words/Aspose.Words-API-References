---
title: FindReplaceOptions.use_substitutions property
linktitle: use_substitutions property
articleTitle: use_substitutions property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.use_substitutions property. Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns"
type: docs
weight: 190
url: /python-net/aspose.words.replacing/findreplaceoptions/use_substitutions/
---

## FindReplaceOptions.use_substitutions property

Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns.
The default value is ``False``.



```python
@property
def use_substitutions(self) -> bool:
    ...

@use_substitutions.setter
def use_substitutions(self, value: bool):
    ...

```

### Remarks

For the details on substitution elements please refer to:
https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.


### Examples

Shows how to recognize and use substitutions within replacement patterns.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Jason gave money to Paul.')
options = aw.replacing.FindReplaceOptions()
options.use_substitutions = True
# Using legacy mode does not support many advanced features, so we need to set it to 'False'.
options.legacy_mode = False
doc.range.replace_regex('([A-z]+) gave money to ([A-z]+)', '$2 took money from $1', options)
self.assertEqual(doc.get_text(), 'Paul took money from Jason.\x0c')
```

Shows how to replace the text with substitutions.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('John sold a car to Paul.')
builder.writeln('Jane sold a house to Joe.')
# We can use a "FindReplaceOptions" object to modify the find-and-replace process.
options = aw.replacing.FindReplaceOptions()
# Set the "use_substitutions" property to "True" to get
# the find-and-replace operation to recognize substitution elements.
# Set the "use_substitutions" property to "False" to ignore substitution elements.
options.use_substitutions = use_substitutions
regex = '([A-z]+) sold a ([A-z]+) to ([A-z]+)'
doc.range.replace_regex(regex, '$3 bought a $2 from $1', options)
if use_substitutions:
    self.assertEqual('Paul bought a car from John.\rJoe bought a house from Jane.', doc.get_text().strip())
else:
    self.assertEqual('$3 bought a $2 from $1.\r$3 bought a $2 from $1.', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)


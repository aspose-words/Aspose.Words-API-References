﻿---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /python-net/aspose.words/style/built_in/
---

## Style.built_in property

True if this style is one of the built-in styles in MS Word.


```python
@property
def built_in(self) -> bool:
    ...

```

### Examples

Shows how to differentiate custom styles from built-in styles.

```python
doc = aw.Document()
# When we create a document using Microsoft Word, or programmatically using Aspose.Words,
# the document will come with a collection of styles to apply to its text to modify its appearance.
# We can access these built-in styles via the document's "Styles" collection.
# These styles will all have the "BuiltIn" flag set to "true".
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# Create a custom style and add it to the collection.
# Custom styles such as this will have the "BuiltIn" flag set to "false".
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)


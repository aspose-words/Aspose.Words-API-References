---
title: built_in property
second_title: Aspose.Words for Python via .NET API Reference
description: "True if this style is one of the built-in styles in MS Word."
type: docs
weight: 30
url: /python-net/aspose.words/style/built_in/
---

## Style.built_in property

True if this style is one of the built-in styles in MS Word.


### Examples

Shows how to differentiate custom styles from built-in styles.

```python
doc = aw.Document()

# When we create a document using Microsoft Word, or programmatically using Aspose.Words,
# the document will come with a collection of styles to apply to its text to modify its appearance.
# We can access these built-in styles via the document's "styles" collection.
# These styles will all have the "built_in" flag set to "True".
style = doc.styles.get_by_name("Emphasis")

self.assertTrue(style.built_in)

# Create a custom style and add it to the collection.
# Custom styles such as this will have the "built_in" flag set to "False".
style = doc.styles.add(aw.StyleType.CHARACTER, "MyStyle")
style.font.color = drawing.Color.navy
style.font.name = "Courier New"

self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)


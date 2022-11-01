---
title: legacy_mode property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a boolean value indicating that old find/replace algorithm is used."
type: docs
weight: 120
url: /python-net/aspose.words.replacing/findreplaceoptions/legacy_mode/
---

## FindReplaceOptions.legacy_mode property

Gets or sets a boolean value indicating that old find/replace algorithm is used.

Use this flag if you need exactly the same behavior as before advanced find/replace feature was introduced.
Note that old algorithm does not support advanced features such as replace with breaks, apply formatting and so on.


### Examples

Shows how to recognize and use substitutions within replacement patterns.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Jason gave money to Paul.")

options = aw.replacing.FindReplaceOptions()
options.use_substitutions = True

# Using legacy mode does not support many advanced features, so we need to set it to 'False'.
options.legacy_mode = False

doc.range.replace_regex(r"([A-z]+) gave money to ([A-z]+)", r"$2 took money from $1", options)

self.assertEqual(doc.get_text(), "Paul took money from Jason.\f")
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)


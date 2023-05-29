---
title: FieldOptions.use_invariant_culture_number_format property
linktitle: use_invariant_culture_number_format property
articleTitle: use_invariant_culture_number_format property
second_title: Aspose.Words for Python
description: "FieldOptions.use_invariant_culture_number_format property. Gets or sets the value indicating that number format is parsed using invariant culture or not"
type: docs
weight: 190
url: /python-net/aspose.words.fields/fieldoptions/use_invariant_culture_number_format/
---

## FieldOptions.use_invariant_culture_number_format property

Gets or sets the value indicating that number format is parsed using invariant culture or not

When this property is set to ``True``, number format is taken from an invariant culture.


When this property is set to ``False``, number format is taken from the current thread's culture.


The default value is ``False``.




### Examples

Shows how to format numbers according to the invariant culture.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

Thread.current_thread.current_culture = "de-DE"
field = builder.insert_field(" = 1234567,89 \\# $#,###,###.##")
field.update()

# Sometimes, fields may not format their numbers correctly under certain cultures.
self.assertFalse(doc.field_options.use_invariant_culture_number_format)
self.assertEqual("$1234567,89 .     ", field.result)

# To fix this, we could change the culture for the entire thread.
# Another way to fix this is to set this flag,
# which gets all fields to use the invariant culture when formatting numbers.
# This way allows us to avoid changing the culture for the entire thread.
doc.field_options.use_invariant_culture_number_format = True
field.update()
self.assertEqual("$1.234.567,89", field.result)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)


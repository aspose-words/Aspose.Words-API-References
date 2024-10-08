﻿---
title: Field.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "Field.type property. Gets the Microsoft Word field type."
type: docs
weight: 100
url: /python-net/aspose.words.fields/field/type/
---

## Field.type property

Gets the Microsoft Word field type.


```python
@property
def type(self) -> aspose.words.fields.FieldType:
    ...

```

### Examples

Shows how to insert a field into a document using a field code.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
field = builder.insert_field('DATE \\@ "dddd, MMMM dd, yyyy"')
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
# This overload of the "insert_field" method automatically updates inserted fields.
self.assertAlmostEqual(datetime.datetime.strptime(field.result, '%A, %B %d, %Y'), datetime.datetime.now(), delta=timedelta(1))
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)


---
title: FieldBuilder constructor
linktitle: FieldBuilder constructor
articleTitle: FieldBuilder constructor
second_title: Aspose.Words for Python
description: "FieldBuilder constructor. Initializes an instance of the [FieldBuilder](../) class."
type: docs
weight: 10
url: /de/python-net/aspose.words.fields/fieldbuilder/__init__/
---

## FieldBuilder(field_type) {#fieldtype}

Initializes an instance of the [FieldBuilder](../) class.



```python
def __init__(self, field_type: aspose.words.fields.FieldType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_type | [FieldType](../../fieldtype/) | The type of the field to build. |

### Examples

Shows how to create and insert a field using a field builder.

```python
doc = aw.Document()
# Eine praktische Methode, Textinhalt zu einem Dokument hinzuzufügen, ist ein Document Builder.
builder = aw.DocumentBuilder(doc)
builder.write(' Hello world! This text is one Run, which is an inline node.')
# Felder haben ihren Builder, den wir verwenden können, um einen Feldcode Stück für Stück zu erstellen.
# In diesem Fall werden wir ein BARCODE-Feld erstellen, das einen US-Postleitzahl darstellt,
# und es dann vor einem Run einfügen.
field_builder = aw.fields.FieldBuilder(aw.fields.FieldType.FIELD_BARCODE)
field_builder.add_argument('90210')
field_builder.add_switch('\\f', 'A')
field_builder.add_switch('\\u')
field_builder.build_and_insert(doc.first_section.body.first_paragraph.runs[0])
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.create_with_field_builder.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldBuilder](../)


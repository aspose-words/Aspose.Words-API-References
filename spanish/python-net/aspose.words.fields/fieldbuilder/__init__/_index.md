---
title: FieldBuilder constructor
linktitle: FieldBuilder constructor
articleTitle: FieldBuilder constructor
second_title: Aspose.Words for Python
description: "FieldBuilder constructor. Initializes an instance of the [FieldBuilder](../) class."
type: docs
weight: 10
url: /es/python-net/aspose.words.fields/fieldbuilder/__init__/
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
# Una forma conveniente de añadir contenido de texto a un documento es con un document builder.
builder = aw.DocumentBuilder(doc)
builder.write(' Hello world! This text is one Run, which is an inline node.')
# Los campos tienen su builder, que podemos usar para construir el código del campo pieza a pieza.
# En este caso, construiremos un campo BARCODE que representa un código postal de EE. UU.,
# y luego lo insertaremos delante de un Run.
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


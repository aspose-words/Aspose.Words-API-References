---
title: Document.normalize_field_types method
linktitle: normalize_field_types method
articleTitle: normalize_field_types method
second_title: Aspose.Words for Python
description: "Document.normalize_field_types method. Changes field type values [FieldChar.field_type](../../../aspose.words.fields/fieldchar/field_type/) of [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) in the whole document so that they correspond to the field types contained in the field codes."
type: docs
weight: 680
url: /it/python-net/aspose.words/document/normalize_field_types/
---

## normalize_field_types() {#default}

Changes field type values [FieldChar.field_type](../../../aspose.words.fields/fieldchar/field_type/) of [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/)
in the whole document so that they correspond to the field types contained in the field codes.



```python
def normalize_field_types(self):
    ...
```

### Remarks

Use this method after document changes that affect field types.

To change field type values in a specific part of the document use [Range.normalize_field_types()](../../range/normalize_field_types/#default).




### Examples

Shows how to get the keep a field's type up to date with its field code.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_code='DATE', field_value=None)
# Aspose.Words rileva automaticamente i tipi di campo in base ai codici di campo.
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
# Modifica manualmente il testo grezzo del campo, che determina il codice del campo.
field_text = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.RUN, True)[0].as_run()
field_text.text = 'PAGE'
# Modificando il codice del campo, questo campo è stato cambiato in uno di tipo diverso,
# ma le proprietà di tipo del campo mostrano ancora il tipo precedente.
self.assertEqual('PAGE', field.get_field_code())
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.start.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.separator.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.end.field_type)
# Aggiorna quelle proprietà con questo metodo per visualizzare il valore corrente.
doc.normalize_field_types()
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.start.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.separator.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.end.field_type)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)


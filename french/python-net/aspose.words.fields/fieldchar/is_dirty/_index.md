---
title: FieldChar.is_dirty property
linktitle: is_dirty property
articleTitle: is_dirty property
second_title: Aspose.Words for Python
description: "FieldChar.is_dirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fields/fieldchar/is_dirty/
---

## FieldChar.is_dirty property

Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications
made to the document.


```python
@property
def is_dirty(self) -> bool:
    ...

@is_dirty.setter
def is_dirty(self, value: bool):
    ...

```

### Examples

Shows how to work with a FieldStart node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.format.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
field_start = field.start
assert field_start.field_type == aw.fields.FieldType.FIELD_DATE
assert field_start.is_dirty == False
assert field_start.is_locked == False
# Récupérez l'objet façade qui représente le champ dans le document.
field = field_start.get_field().as_field_date()
assert field.is_locked == False
assert field.get_field_code() == ' DATE  \\@ "dddd, MMMM dd, yyyy"'
# Mettez à jour le champ pour afficher la date actuelle.
field.update()
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldChar](../)


---
title: Paragraph.append_field method
linktitle: append_field method
articleTitle: append_field method
second_title: Aspose.Words for Python
description: "aspose.words.Paragraph.append_field method"
type: docs
weight: 260
url: /fr/python-net/aspose.words/paragraph/append_field/
---

## append_field(field_type, update_field) {#fieldtype_bool}

Appends a field to this paragraph.


```python
def append_field(self, field_type: aspose.words.fields.FieldType, update_field: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_type | [FieldType](../../../aspose.words.fields/fieldtype/) | The type of the field to append. |
| update_field | bool | Specifies whether to update the field immediately. |

### Returns

A [Field](../../../aspose.words.fields/field/) object that represents the appended field.


## append_field(field_code) {#str}

Appends a field to this paragraph.


```python
def append_field(self, field_code: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_code | str | The field code to append (without curly braces). |

### Returns

A [Field](../../../aspose.words.fields/field/) object that represents the appended field.


## append_field(field_code, field_value) {#str_str}

Appends a field to this paragraph.


```python
def append_field(self, field_code: str, field_value: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_code | str | The field code to append (without curly braces). |
| field_value | str | The field value to append. Pass ``None`` for fields that do not have a value. |

### Returns

A [Field](../../../aspose.words.fields/field/) object that represents the appended field.


## Examples

Shows various ways of appending fields to a paragraph.

```python
doc = aw.Document()
paragraph = doc.first_section.body.first_paragraph
# Voici trois façons d'ajouter un champ à la fin d'un paragraphe.
# 1 -  Ajouter un champ DATE en utilisant un type de champ, puis le mettre à jour :
paragraph.append_field(aw.fields.FieldType.FIELD_DATE, True)
# 2 -  Ajouter un champ HEURE en utilisant un code de champ :
paragraph.append_field(' TIME  \\@ "HH:mm:ss" ')
# 3 -  Ajouter un champ CITATION en utilisant un code de champ, et le faire afficher une valeur de substitution :
paragraph.append_field(' QUOTE "Real value"', 'Placeholder value')
self.assertEqual('Placeholder value', doc.range.fields[2].result)
# Ce champ affichera sa valeur de substitution jusqu'à ce que nous le mettions à jour.
doc.update_fields()
self.assertEqual('Real value', doc.range.fields[2].result)
doc.save(ARTIFACTS_DIR + 'Paragraph.append_field.docx')
```

## See Also

* module [aspose.words](../../)
* class [Paragraph](../)


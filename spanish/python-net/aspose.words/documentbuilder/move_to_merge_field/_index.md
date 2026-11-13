---
title: DocumentBuilder.move_to_merge_field method
linktitle: move_to_merge_field method
articleTitle: move_to_merge_field method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.move_to_merge_field method"
type: docs
weight: 590
url: /es/python-net/aspose.words/documentbuilder/move_to_merge_field/
---

## move_to_merge_field(field_name) {#str}

Moves the cursor to a position just beyond the specified merge field and removes the merge field.


```python
def move_to_merge_field(self, field_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_name | str | The case-insensitive name of the mail merge field. |

### Remarks

Note that this method deletes the merge field from the document after moving the cursor.




### Returns

``True`` if the merge field was found and the cursor was moved; ``False`` otherwise.


## move_to_merge_field(field_name, is_after, is_delete_field) {#str_bool_bool}

Moves the merge field to the specified merge field.


```python
def move_to_merge_field(self, field_name: str, is_after: bool, is_delete_field: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_name | str | The case-insensitive name of the mail merge field. |
| is_after | bool | When ``True``, moves the cursor to be after the field end. When ``False``, moves the cursor to be before the field start.  |
| is_delete_field | bool | When ``True``, deletes the merge field. |

### Returns

``True`` if the merge field was found and the cursor was moved; ``False`` otherwise.


## Examples

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte algunos MERGEFIELDS, que aceptan datos de columnas con el mismo nombre en una fuente de datos durante una combinación de correspondencia,
# y luego complételos manualmente.
builder.insert_field(field_code=' MERGEFIELD Chairman ')
builder.insert_field(field_code=' MERGEFIELD ChiefFinancialOfficer ')
builder.insert_field(field_code=' MERGEFIELD ChiefTechnologyOfficer ')
builder.move_to_merge_field(field_name='Chairman')
builder.bold = True
builder.writeln('John Doe')
builder.move_to_merge_field(field_name='ChiefFinancialOfficer')
builder.italic = True
builder.writeln('Jane Doe')
builder.move_to_merge_field(field_name='ChiefTechnologyOfficer')
builder.italic = True
builder.writeln('John Bloggs')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.FillMergeFields.docx')
```

Shows how to insert fields, and move the document builder's cursor to them.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_field(field_code='MERGEFIELD MyMergeField1 \\* MERGEFORMAT')
builder.insert_field(field_code='MERGEFIELD MyMergeField2 \\* MERGEFORMAT')
# Mueva el cursor al primer MERGEFIELD.
builder.move_to_merge_field(field_name='MyMergeField1', is_after=True, is_delete_field=False)
# Observe que el cursor se coloca inmediatamente después del primer MERGEFIELD, y antes del segundo.
self.assertEqual(doc.range.fields[1].start, builder.current_node)
self.assertEqual(doc.range.fields[0].end, builder.current_node.previous_sibling)
# Si deseamos editar el código de campo o el contenido del campo usando el builder,
# su cursor tendría que estar dentro de un campo.
# Para colocarlo dentro de un campo, necesitaríamos llamar al método MoveTo del document builder.
# y pasar el nodo de inicio o separador del campo como argumento.
builder.write(' Text between our merge fields. ')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.MergeFields.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)


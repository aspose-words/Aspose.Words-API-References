---
title: DocumentBuilder.move_to_merge_field method
linktitle: move_to_merge_field method
articleTitle: move_to_merge_field method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.move_to_merge_field method"
type: docs
weight: 590
url: /tr/python-net/aspose.words/documentbuilder/move_to_merge_field/
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
# Posta birleştirme sırasında veri kaynağındaki aynı ada sahip sütunlardan veri kabul eden bazı MERGEFIELDS ekleyin,
# ve ardından bunları manuel olarak doldurun.
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
# İmleci ilk MERGEFIELD'e taşıyın.
builder.move_to_merge_field(field_name='MyMergeField1', is_after=True, is_delete_field=False)
# İmlecin ilk MERGEFIELD'den hemen sonra ve ikinciden önce konumlandırıldığını unutmayın.
self.assertEqual(doc.range.fields[1].start, builder.current_node)
self.assertEqual(doc.range.fields[0].end, builder.current_node.previous_sibling)
# Alan kodunu veya içeriğini oluşturucu kullanarak düzenlemek istersek,
# imlecinin bir alanın içinde olması gerekir.
# Bunu bir alanın içine yerleştirmek için belge oluşturucusunun MoveTo metodunu çağırmamız gerekir
# ve alanın başlangıç veya ayırıcı düğümünü bir argüman olarak geçirin.
builder.write(' Text between our merge fields. ')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.MergeFields.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)


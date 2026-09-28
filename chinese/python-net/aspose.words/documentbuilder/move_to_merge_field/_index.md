---
title: DocumentBuilder.move_to_merge_field method
linktitle: move_to_merge_field method
articleTitle: move_to_merge_field method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.move_to_merge_field method"
type: docs
weight: 590
url: /zh/python-net/aspose.words/documentbuilder/move_to_merge_field/
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
# 插入一些 MERGEFIELDS，这些字段在邮件合并期间接受来自数据源中同名列的数据，
# 然后手动填充它们。
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
# 将光标移动到第一个 MERGEFIELD。
builder.move_to_merge_field(field_name='MyMergeField1', is_after=True, is_delete_field=False)
# 请注意，光标被放置在第一个 MERGEFIELD 之后、第二个 MERGEFIELD 之前。
self.assertEqual(doc.range.fields[1].start, builder.current_node)
self.assertEqual(doc.range.fields[0].end, builder.current_node.previous_sibling)
# 如果我们希望使用生成器编辑字段的字段代码或内容，
# 光标需要位于字段内部。
# 要将其放置在字段内部，我们需要调用文档生成器的 MoveTo 方法。
# 并将字段的起始或分隔节点作为参数传递。
builder.write(' Text between our merge fields. ')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.MergeFields.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)


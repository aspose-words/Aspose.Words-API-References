---
title: FieldAuthor class
linktitle: FieldAuthor class
articleTitle: FieldAuthor class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldAuthor class. Implements the AUTHOR field"
type: docs
weight: 110
url: /zh/python-net/aspose.words.fields/fieldauthor/
---

## FieldAuthor class

Implements the AUTHOR field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Retrieves, and optionally sets, the document author's name, as recorded in the **Author** property of the
built-in document properties.



**Inheritance:** [FieldAuthor](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldAuthor()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [author_name](./author_name/) | Gets or sets the document author's name. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to use an AUTHOR field to display a document creator's name.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# AUTHOR 字段从名为 "Author" 的内置文档属性获取结果。
# 如果我们在 Microsoft Word 中创建并保存文档，
# 该属性中将会是我们的用户名。
# 然而，如果我们使用 Aspose.Words 以编程方式创建文档，
# 默认情况下，"Author" 属性将是空字符串。
self.assertEqual('', doc.built_in_document_properties.author)
# 设置 AUTHOR 字段使用的备用作者名称
# 如果 "Author" 属性包含空字符串。
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# 更新包含值的 AUTHOR 字段
# 将把该值应用到 "Author" 内置属性。
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# 更改此属性后，再更新 AUTHOR 字段将把该值应用到字段。
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# 如果我们在更改其 "Name" 属性后更新 AUTHOR 字段，
# 则字段将显示新名称并将新名称应用到内置属性。
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# AUTHOR 字段不会影响 DefaultDocumentAuthor 属性。
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)


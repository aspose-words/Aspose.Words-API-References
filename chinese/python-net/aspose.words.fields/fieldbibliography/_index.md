---
title: FieldBibliography class
linktitle: FieldBibliography class
articleTitle: FieldBibliography class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldBibliography class. Implements the BIBLIOGRAPHY field"
type: docs
weight: 180
url: /zh/python-net/aspose.words.fields/fieldbibliography/
---

## FieldBibliography class

Implements the BIBLIOGRAPHY field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Inserts the contents of the document's Bibliography part in a bibliographic style.


**Inheritance:** [FieldBibliography](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldBibliography()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [filter_language_id](./filter_language_id/) | Gets or sets the language ID that is used to filter the bibliographic data to only the sources in the document that use that language. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [format_language_id](./format_language_id/) | Gets or sets the language ID that is used to format the bibliographic sources in the document. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [source_tag](./source_tag/) | Gets or sets a value so that only the sources with matching Tag element value are displayed in the bibliography. |
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

Shows how to work with CITATION and BIBLIOGRAPHY fields.

```python
# 打开一个包含参考文献来源的文档，我们可以在其中找到
# Microsoft Word 的“引用”→“文献目录与参考文献”→“管理来源”。
doc = aw.Document(MY_DIR + 'Bibliography.docx')
builder = aw.DocumentBuilder(doc)
builder.write('Text to be cited with one source.')
# 创建仅包含页码和被引用书籍作者的引文。
field_citation = builder.insert_field(aw.fields.FieldType.FIELD_CITATION, True).as_field_citation()
# 我们使用它们的标签名称来引用来源。
field_citation.source_tag = 'Book1'
field_citation.page_number = '85'
field_citation.suppress_author = False
field_citation.suppress_title = True
field_citation.suppress_year = True
self.assertEqual(' CITATION  Book1 \\p 85 \\t \\y', field_citation.get_field_code())
# 创建一个更详细的引用，其中引用了两个来源。
builder.insert_paragraph()
builder.write('Text to be cited with two sources.')
field_citation = builder.insert_field(aw.fields.FieldType.FIELD_CITATION, True).as_field_citation()
field_citation.source_tag = 'Book1'
field_citation.another_source_tag = 'Book2'
field_citation.format_language_id = 'en-US'
field_citation.page_number = '19'
field_citation.prefix = 'Prefix '
field_citation.suffix = ' Suffix'
field_citation.suppress_author = False
field_citation.suppress_title = False
field_citation.suppress_year = False
field_citation.volume_number = 'VII'
self.assertEqual(' CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f "Prefix " \\s " Suffix" \\v VII', field_citation.get_field_code())
# 我们可以使用 BIBLIOGRAPHY 字段来显示文档中的所有来源。
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_bibliography = builder.insert_field(aw.fields.FieldType.FIELD_BIBLIOGRAPHY, True).as_field_bibliography()
field_bibliography.format_language_id = '5129'
self.assertEqual(' BIBLIOGRAPHY  \\l 5129', field_bibliography.get_field_code())
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_citation.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)


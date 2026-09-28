---
title: FieldToa class
linktitle: FieldToa class
articleTitle: FieldToa class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToa class. Implements the TOA field"
type: docs
weight: 1060
url: /zh/python-net/aspose.words.fields/fieldtoa/
---

## FieldToa class

Implements the TOA field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Builds a table of authorities (that is, a list of the references in a legal document, such as references
to cases, statutes, and rules, along with the numbers of the pages on which the references appear) using the
entries specified by TA fields.


**Inheritance:** [FieldToa](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldToa()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_category](./entry_category/) | Gets or sets the integral category for entries included in the table. |
| [entry_separator](./entry_separator/) | Gets or sets the character sequence that is used to separate a table of authorities entry and its page number. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [page_number_list_separator](./page_number_list_separator/) | Gets or sets the character sequence that is used to separate two page numbers in a page number list. |
| [page_range_separator](./page_range_separator/) | Gets or sets the character sequence that is used to separate the start and end of a page range. |
| [remove_entry_formatting](./remove_entry_formatting/) | Gets or sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_name](./sequence_name/) | Gets or sets the name of a sequence whose number is included with the page number. |
| [sequence_separator](./sequence_separator/) | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [use_heading](./use_heading/) | Gets or sets whether to include the category heading for the entries in a table of authorities. |
| [use_passim](./use_passim/) | Gets or sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |

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

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一个 TOA 字段，它将在文档中为每个 TA 字段创建一个条目，
# 为每个条目显示长引文和页码。
field_toa = builder.insert_field(field_type=FieldType.FIELD_TOA, update_field=False).as_field_toa()
# 设置我们表格的条目类别。此 TOA 现在只会包含 TA 字段
# 其 EntryCategory 属性具有匹配值的字段。
field_toa.entry_category = '1'
# 此外，索引 1 处的权威目录类别是 "Cases"，
# 如果我们将此变量设为 true，它将显示为我们表格的标题。
field_toa.use_heading = True
# 我们可以通过命名书签进一步过滤 TA 字段，使其必须位于 TOA 范围内。
field_toa.bookmark_name = 'MyBookmark'
# 默认情况下，在 TA 字段的引文之间会出现跨页的点线制表符
# 以及其页码。我们可以用此属性中放置的任意文本替换它。
# 插入制表符字符将保留原始制表符。
field_toa.entry_separator = ' \t p.'
# 如果我们有多个共享相同长引文的 TA 条目，
# 它们各自的页码将显示在同一行。
# 我们可以使用此属性指定一个字符串，用于分隔它们的页码。
field_toa.page_number_list_separator = ' & p. '
# 我们可以将其设为 true，以使我们的表格显示单词 "passim"
# 如果一行中有五个或更多页码。
field_toa.use_passim = True
# 一个 TA 字段可以引用一段页码范围。
# 我们可以在此指定一个字符串，以出现在此类范围的起始页码和结束页码之间。
field_toa.page_range_separator = ' to '
# TA 字段的格式将传递到我们的表格中。
# 我们可以通过设置 RemoveEntryFormatting 标志来禁用此功能。
field_toa.remove_entry_formatting = True
builder.font.color = Color.green
builder.font.name = 'Arial Black'
self.assertEqual(' TOA  \\c 1 \\h \\b MyBookmark \\e " \t p." \\l " & p. " \\p \\g " to " \\f', field_toa.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 此 TA 字段不会作为条目出现在 TOA 中，因为它位于
# TOA 的 BookmarkName 属性指定的书签范围之外。
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 1')
self.assertEqual(' TA  \\c 1 \\l "Source 1"', field_ta.get_field_code())
# 此 TA 字段位于书签内部，
# 但条目类别与表格的不匹配，因此 TA 字段不会包含它。
builder.start_bookmark('MyBookmark')
field_ta = ExField._insert_toa_entry(builder, '2', 'Source 2')
# 此条目将出现在表格中。
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
# TOA 表格不显示简短引用，
# 但我们可以将它们用作简写，以引用多个 TA 字段引用的冗长来源名称。
field_ta.short_citation = 'S.3'
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\s S.3', field_ta.get_field_code())
# 我们可以使用以下属性将页码设置为粗体/斜体。
# 如果我们将表格设置为忽略格式，仍然会看到这些效果。
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 2')
field_ta.is_bold = True
field_ta.is_italic = True
self.assertEqual(' TA  \\c 1 \\l "Source 2" \\b \\i', field_ta.get_field_code())
# 我们可以配置 TA 字段，使其 TOA 条目引用书签跨越的页码范围。
# 请注意，此条目引用与上面相同的来源，以在我们的表格中共享一行。
# 此行将包含上面条目的页码以及此条目的页码范围，
# 并在页码之间使用表格的页码列表和页码范围分隔符。
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
field_ta.page_range_bookmark_name = 'MyMultiPageBookmark'
builder.start_bookmark('MyMultiPageBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.end_bookmark('MyMultiPageBookmark')
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\r MyMultiPageBookmark', field_ta.get_field_code())
# 如果我们已启用表格的 "Passim" 功能，拥有 5 条或更多具有相同来源的 TA 条目将触发它。
i = 0
while i < 5:
    ExField._insert_toa_entry(builder, '1', 'Source 4')
    i += 1
builder.end_bookmark('MyBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOA.TA.docx')
```

Shows how to build and customize a table of authorities using TOA and TA fields (InsertToaEntry).

```python
@staticmethod
def _insert_toa_entry(builder, entry_category, long_citation):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOA_ENTRY, update_field=False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    return field
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)


---
title: FieldToc class
linktitle: FieldToc class
articleTitle: FieldToc class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToc class. Implements the TOC field"
type: docs
weight: 1070
url: /zh/python-net/aspose.words.fields/fieldtoc/
---

## FieldToc class

Implements the TOC field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Builds a table of contents (which can also be a table of figures) using the entries specified by TC fields,
their heading levels, and specified styles, and inserts that table at this place in the document.


**Inheritance:** [FieldToc](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldToc()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [captionless_table_of_figures_label](./captionless_table_of_figures_label/) | Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [custom_styles](./custom_styles/) | Gets or sets a list of styles other than the built-in heading styles to include in the table of contents. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_identifier](./entry_identifier/) | Gets or sets a string that should match type identifiers of TC fields being included. |
| [entry_level_range](./entry_level_range/) | Gets or sets a range of levels of the table of contents entries to be included. |
| [entry_separator](./entry_separator/) | Gets or sets a sequence of characters that separate an entry and its page number. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [heading_level_range](./heading_level_range/) | Gets or sets a range of heading levels to include. |
| [hide_in_web_layout](./hide_in_web_layout/) | Gets or sets whether to hide tab leader and page numbers in Web layout view. |
| [insert_hyperlinks](./insert_hyperlinks/) | Gets or sets whether to make the table of contents entries hyperlinks. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [page_number_omitting_level_range](./page_number_omitting_level_range/) | Gets or sets a range of levels of the table of contents entries from which to omits page numbers. |
| [prefixed_sequence_identifier](./prefixed_sequence_identifier/) | Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [preserve_line_breaks](./preserve_line_breaks/) | Gets or sets whether to preserve newline characters within table entries. |
| [preserve_tabs](./preserve_tabs/) | Gets or sets whether to preserve tab entries within table entries. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_separator](./sequence_separator/) | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [table_of_figures_label](./table_of_figures_label/) | Gets or sets the name of the sequence identifier used when building a table of figures. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [use_paragraph_outline_level](./use_paragraph_outline_level/) | Gets or sets whether to use the applied paragraph outline level. |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update_page_numbers()](./update_page_numbers/#default) | Updates the page numbers for items in this table of contents. |

### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
# 插入一个目录（TOC）字段，它会将所有标题汇总到目录中。
# 对于每个标题，此字段将在左侧创建一行，文本使用该标题样式，
# 右侧显示标题所在的页码。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# 使用 BookmarkName 属性仅列出标题
# 仅列出位于名为 "MyBookmark" 的书签范围内的标题。
field.bookmark_name = 'MyBookmark'
# 带有内置标题样式（例如 "Heading 1"）的文本将被视为标题。
# 我们可以在此属性中指定其他样式，使其被目录识别为标题，并设定其目录层级。
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# 默认情况下，Styles/TOC 层级在 CustomStyles 属性中以逗号分隔，
# 但我们可以在此属性中设置自定义分隔符。
doc.field_options.custom_toc_style_separator = ';'
# 配置字段以排除任何目录层级超出此范围的标题。
field.heading_level_range = '1-3'
# 目录将不显示目录层级在此范围内的标题的页码。
field.page_number_omitting_level_range = '2-5'
# 设置自定义字符串，以分隔每个标题与其页码。
field.entry_separator = '-'
field.insert_hyperlinks = True
field.hide_in_web_layout = False
field.preserve_line_breaks = True
field.preserve_tabs = True
field.use_paragraph_outline_level = False
self.insert_new_page_with_heading(builder, 'First entry', 'Heading 1')
builder.writeln('Paragraph text.')
self.insert_new_page_with_heading(builder, 'Second entry', 'Heading 1')
self.insert_new_page_with_heading(builder, 'Third entry', 'Quote')
self.insert_new_page_with_heading(builder, 'Fourth entry', 'Intense Quote')
# 这两个标题的页码将被省略，因为它们位于 "2-5" 范围内。
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# 此条目不会出现，因为 "Heading 4" 超出了我们之前设置的 "1-3" 范围。
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# 此条目未显示，因为它位于目录指定的书签之外。
self.insert_new_page_with_heading(builder, 'Eighth entry', 'Heading 1')
self.assertEqual(' TOC  \\b MyBookmark \\t "Quote; 6; Intense Quote; 7" \\o 1-3 \\n 2-5 \\p - \\h \\u0000 \\w', field.get_field_code())
field.update_page_numbers()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.docx')
```

Shows how to insert a TOC, and populate it with entries based on heading styles (InsertNewPageWithHeading).

```python
def insert_new_page_with_heading(self, builder, caption_text, style_name):
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    original_style = builder.paragraph_format.style_name
    builder.paragraph_format.style = builder.document.styles.get_by_name(style_name)
    builder.writeln(caption_text)
    builder.paragraph_format.style = builder.document.styles.get_by_name(original_style)
```

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# TOC 域可以为文档中找到的每个 SEQ 域在目录中创建一个条目。
# 每个条目包含包含 SEQ 域的段落以及该域所在页的页码。
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# SEQ 域显示一个在每个 SEQ 域递增的计数。
# 这些域还为每个唯一命名的序列维护单独的计数
# 由 SEQ 域的 "SequenceIdentifier" 属性标识。
# 使用 "TableOfFiguresLabel" 属性为 TOC 命名主序列。
# 现在，此 TOC 只会从其 "SequenceIdentifier" 设置为 "MySequence" 的 SEQ 域创建条目。
field_toc.table_of_figures_label = 'MySequence'
# 我们可以在 "PrefixedSequenceIdentifier" 属性中为另一个 SEQ 域序列命名。
# 来自此前缀序列的 SEQ 域将不会创建 TOC 条目。
# 现在，从主序列 SEQ 域创建的每个 TOC 条目还将显示计数
# 前缀序列当前位于生成该条目的主序列 SEQ 字段上。
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# 每个目录条目将在左侧立即显示前缀序列计数
# 页面编号的左侧，即主序列 SEQ 字段出现的页码。
# 我们可以指定一个自定义分隔符，以显示在这两个数字之间。
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 使用 SEQ 字段填充此目录有两种方法。
# 1 - 插入属于目录前缀序列的 SEQ 字段：
# 此字段将把 "PrefixSequence" 的 SEQ 序列计数增加 1。
# 由于此字段不属于已标识的主序列
# 由目录的 "TableOfFiguresLabel" 属性标识，它将不会作为条目出现。
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 - 插入属于目录主序列的 SEQ 字段：
# 此 SEQ 字段将在目录中创建一个条目。
# 目录条目将包含 SEQ 字段所在的段落以及它出现的页码。
# 此条目还将显示当前前缀序列的计数，
# 该计数与页码之间由目录的 SeqenceSeparator 属性的值分隔。
# "PrefixSequence" 计数为 1，主序列 SEQ 字段位于第 2 页，
# 分隔符为 ">"，因此条目将显示为 "1>2"。
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# 插入一页，将前缀序列前进 2，并随后插入 SEQ 字段以创建目录条目。
# 前缀序列现在为 2，主序列 SEQ 字段位于第 3 页，
# 因此目录条目将在页码处显示 "2>3"。
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
builder.write('Second TOC entry, MySequence #')
field_seq.sequence_identifier = 'MySequence'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.SEQ.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)


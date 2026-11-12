---
title: FieldToc class
linktitle: FieldToc class
articleTitle: FieldToc class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToc class. Implements the TOC field"
type: docs
weight: 1070
url: /ru/python-net/aspose.words.fields/fieldtoc/
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
# Вставьте поле Оглавления (TOC), которое соберёт все заголовки в таблицу содержимого.
# Для каждого заголовка это поле создаст строку с текстом в стиле этого заголовка слева,
# а номер страницы, на которой находится заголовок, — справа.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Используйте свойство BookmarkName, чтобы перечислять только заголовки
# которые находятся в пределах закладки с именем "MyBookmark".
field.bookmark_name = 'MyBookmark'
# Текст с встроенным стилем заголовка, например "Heading 1", применённый к нему, будет считаться заголовком.
# Мы можем указать дополнительные стили, которые будут распознаны как заголовки Оглавлением (TOC) в этом свойстве, и их уровни Оглавления.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# По умолчанию стили/уровни Оглавления разделяются в свойстве CustomStyles запятой,
# но мы можем задать пользовательский разделитель в этом свойстве.
doc.field_options.custom_toc_style_separator = ';'
# Настройте поле, чтобы исключить любые заголовки, у которых уровни Оглавления находятся за пределами этого диапазона.
field.heading_level_range = '1-3'
# Оглавление не будет отображать номера страниц заголовков, уровни Оглавления которых находятся в этом диапазоне.
field.page_number_omitting_level_range = '2-5'
# Установите пользовательскую строку, которая будет разделять каждый заголовок и его номер страницы.
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
# Эти два заголовка будут без номеров страниц, потому что они находятся в диапазоне "2-5".
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# Эта запись не отображается, потому что "Heading 4" находится за пределами диапазона "1-3", установленного ранее.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# Эта запись не отображается, потому что она находится за пределами закладки, указанной в оглавлении.
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
# Поле TOC может создавать запись в своем оглавлении для каждого найденного в документе поля SEQ.
# Каждая запись содержит абзац, включающий поле SEQ, и номер страницы, на которой появляется поле.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Поля SEQ отображают счётчик, который увеличивается у каждого поля SEQ.
# Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности
# идентифицируемой свойством "SequenceIdentifier" поля SEQ.
# Используйте свойство "TableOfFiguresLabel", чтобы задать основную последовательность для TOC.
# Теперь этот TOC будет создавать записи только из полей SEQ, у которых свойство "SequenceIdentifier" установлено в "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Мы можем задать другую последовательность полей SEQ в свойстве "PrefixedSequenceIdentifier".
# Поля SEQ из этой префиксной последовательности не будут создавать записи в TOC.
# Каждая запись TOC, созданная из поля SEQ основной последовательности, теперь также будет отображать счётчик, который
# префиксная последовательность в данный момент находится в основном поле SEQ последовательности, которое создало запись.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Каждая запись оглавления будет отображать количество префиксной последовательности сразу слева.
# от номера страницы, на которой находится основное поле SEQ последовательности.
# Мы можем указать пользовательский разделитель, который будет отображаться между этими двумя числами.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Существует два способа использования полей SEQ для заполнения этого оглавления.
# 1 - Вставка поля SEQ, принадлежащего префиксной последовательности оглавления:
# Это поле увеличит счётчик последовательности SEQ для "PrefixSequence" на 1.
# Поскольку это поле не принадлежит основной последовательности, идентифицированной
# свойством "TableOfFiguresLabel" оглавления, оно не будет отображаться как запись.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 - Вставка поля SEQ, принадлежащего основной последовательности оглавления:
# Это поле SEQ создаст запись в оглавлении.
# Запись оглавления будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно отображается.
# Эта запись также будет показывать текущее значение префиксной последовательности,
# отделённое от номера страницы значением свойства SeqenceSeparator оглавления.
# Значение "PrefixSequence" равно 1, это основное поле SEQ находится на странице 2,
# а разделитель — ">", поэтому запись будет отображать "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Вставьте страницу, увеличьте префиксную последовательность на 2 и вставьте поле SEQ, чтобы затем создать запись в оглавлении.
# Префиксная последовательность теперь равна 2, а основное поле SEQ находится на странице 3,
# поэтому запись оглавления будет отображать "2>3" в счётчике страниц.
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


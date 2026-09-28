---
title: FieldToc class
linktitle: FieldToc class
articleTitle: FieldToc class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToc class. Implements the TOC field"
type: docs
weight: 1070
url: /ar/python-net/aspose.words.fields/fieldtoc/
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
# أدرج حقل فهرس المحتويات (TOC)، والذي سيجمع جميع العناوين في جدول المحتويات.
# لكل عنوان، سيُنشئ هذا الحقل سطرًا بالنص بتنسيق ذلك العنوان إلى اليسار،
# والصفحة التي يظهر فيها العنوان إلى اليمين.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# استخدم خاصية BookmarkName لتسرد العناوين فقط
# التي تظهر ضمن حدود إشارة مرجعية باسم "MyBookmark".
field.bookmark_name = 'MyBookmark'
# النص الذي يحتوي على نمط عنوان مدمج، مثل "Heading 1"، سيُعد كعنوان.
# يمكننا تسمية أنماط إضافية لتُلتقط كعناوين بواسطة الفهرس في هذه الخاصية ومستويات الفهرس الخاصة بها.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# بشكل افتراضي، يتم فصل مستويات الأنماط/الفهرس في خاصية CustomStyles بفاصلة،
# ولكن يمكننا تعيين فاصل مخصص في هذه الخاصية.
doc.field_options.custom_toc_style_separator = ';'
# قم بتكوين الحقل لاستبعاد أي عناوين لها مستويات فهرس خارج هذا النطاق.
field.heading_level_range = '1-3'
# لن يعرض الفهرس أرقام صفحات العناوين التي مستويات فهرسها ضمن هذا النطاق.
field.page_number_omitting_level_range = '2-5'
# حدد سلسلة مخصصة تفصل كل عنوان عن رقم صفحته.
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
# سيتم حذف أرقام الصفحات لهذين العنوانين لأنهما ضمن النطاق "2-5".
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# هذا الإدخال لا يظهر لأن "Heading 4" خارج النطاق "1-3" الذي حددناه مسبقًا.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# هذا الإدخال لا يظهر لأنه خارج العلامة المرجعية المحددة بواسطة جدول المحتويات.
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
# يمكن لحقل TOC إنشاء إدخال في جدول المحتويات لكل حقل SEQ موجود في المستند.
# كل إدخال يحتوي على الفقرة التي تشمل حقل SEQ ورقم الصفحة التي يظهر فيها الحقل.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# حقول SEQ تعرض عدًّا يزداد عند كل حقل SEQ.
# هذه الحقول تحافظ أيضًا على عدادات منفصلة لكل تسلسل مسمى فريد
# محددة بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
# استخدم خاصية "TableOfFiguresLabel" لتسمية تسلسل رئيسي للـ TOC.
# الآن، سيقوم هذا الـ TOC بإنشاء إدخالات فقط من حقول SEQ التي تم تعيين "SequenceIdentifier" لها إلى "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# يمكننا تسمية تسلسل حقل SEQ آخر في خاصية "PrefixedSequenceIdentifier".
# حقول SEQ من هذا التسلسل المسبق لن تنشئ إدخالات TOC.
# كل إدخال TOC تم إنشاؤه من حقل SEQ لتسلسل رئيسي سيعرض الآن أيضًا العد الذي
# التسلسل السابق حاليًا في حقل SEQ التسلسل الأساسي الذي أنشأ الإدخال.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# سيعرض كل إدخال TOC عدد التسلسل السابق مباشرةً إلى اليسار
# من رقم الصفحة التي يظهر فيها حقل SEQ التسلسل الرئيسي.
# يمكننا تحديد فاصل مخصص سيظهر بين هذين الرقمين.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# هناك طريقتان لاستخدام حقول SEQ لملء هذا TOC.
# 1 - إدراج حقل SEQ ينتمي إلى تسلسل البادئة في TOC:
# سيزيد هذا الحقل عدد تسلسل SEQ لـ "PrefixSequence" بمقدار 1.
# نظرًا لأن هذا الحقل لا ينتمي إلى التسلسل الرئيسي المحدد
# بواسطة خاصية "TableOfFiguresLabel" في TOC، لن يظهر كإدخال.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 - إدراج حقل SEQ ينتمي إلى التسلسل الرئيسي في TOC:
# سيُنشئ حقل SEQ هذا إدخالًا في TOC.
# سيتضمن إدخال TOC الفقرة التي يوجد فيها حقل SEQ ورقم الصفحة التي يظهر فيها.
# سيعرض هذا الإدخال أيضًا العدد الذي وصل إليه التسلسل السابق حاليًا،
# مفصولًا عن رقم الصفحة بالقيمة الموجودة في خاصية SeqenceSeparator في TOC.
# العدد "PrefixSequence" هو 1، وحقل SEQ التسلسل الرئيسي على الصفحة 2،
# والفاصل هو ">"، لذا سيعرض الإدخال "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# أدرج صفحة، وقدم التسلسل السابق بمقدار 2، ثم أدرج حقل SEQ لإنشاء إدخال TOC لاحقًا.
# التسلسل السابق الآن هو 2، وحقل SEQ التسلسل الرئيسي على الصفحة 3،
# لذا سيعرض إدخال TOC "2>3" في عدد صفحته.
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


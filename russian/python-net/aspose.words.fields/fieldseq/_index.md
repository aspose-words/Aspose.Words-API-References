---
title: FieldSeq class
linktitle: FieldSeq class
articleTitle: FieldSeq class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSeq class. Implements the SEQ field"
type: docs
weight: 930
url: /ru/python-net/aspose.words.fields/fieldseq/
---

## FieldSeq class

Implements the SEQ field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Sequentially numbers chapters, tables, figures, and other user-defined lists of items in a document.


**Inheritance:** [FieldSeq](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSeq()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_next_number](./insert_next_number/) | Gets or sets whether to insert the next sequence number for the specified item. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [reset_heading_level](./reset_heading_level/) | Gets or sets an integer number representing a heading level to reset the sequence number to. Returns -1 if the number is absent. |
| [reset_number](./reset_number/) | Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_identifier](./sequence_identifier/) | Gets or sets the name assigned to the series of items that are to be numbered. |
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

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Поля SEQ отображают счётчик, который увеличивается у каждого поля SEQ.
# Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности
# идентифицируемой свойством "SequenceIdentifier" поля SEQ.
# Вставьте поле SEQ, которое будет отображать текущее значение счётчика "MySequence",
# после использования свойства "ResetNumber" для установки его в 100.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Отобразите следующее число в этой последовательности с помощью другого поля SEQ.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Вставьте заголовок уровня 1.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Вставьте ещё одно поле SEQ из той же последовательности и настройте его сбрасывать счётчик до 1 при каждом заголовке.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# Указанный выше заголовок — заголовок уровня 1, поэтому счётчик этой последовательности сбрасывается до 1.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Перейдите к следующему номеру этой последовательности.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.insert_next_number = True
field_seq.update()
self.assertEqual(' SEQ  MySequence \\n', field_seq.get_field_code())
self.assertEqual('2', field_seq.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.ResetNumbering.docx')
```

Shows how to combine table of contents and sequence fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Поле TOC может создавать запись в своем оглавлении для каждого найденного в документе поля SEQ.
# Каждая запись содержит абзац, в котором находится поле SEQ,
# и номер страницы, на которой появляется поле.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Настройте это поле TOC так, чтобы у него было свойство SequenceIdentifier со значением "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Настройте это поле TOC так, чтобы оно выбирало только поля SEQ, находящиеся в пределах закладки
# с именем "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# Поля SEQ отображают счётчик, который увеличивается у каждого поля SEQ.
# Эти поля также поддерживают отдельные счётчики для каждой уникальной именованной последовательности
# идентифицируемой свойством "SequenceIdentifier" поля SEQ.
# Вставьте поле SEQ с идентификатором последовательности, соответствующим полю TOC
# TableOfFiguresLabel. Это поле не создаст запись в TOC, поскольку оно находится за пределами
# границ закладки, обозначенных "BookmarkName".
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# Последовательность этого поля SEQ соответствует свойству TOC "TableOfFiguresLabel" и находится в пределах границ закладки.
# Абзац, содержащий это поле, появится в TOC как запись.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# Последовательность этого поля SEQ не соответствует свойству TOC "TableOfFiguresLabel",
# но находится в пределах границ закладки. Его абзац не появится в TOC как запись.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# Последовательность этого поля SEQ соответствует свойству TOC "TableOfFiguresLabel" и находится в пределах границ закладки.
# Это поле также ссылается на другую закладку. Содержимое этой закладки появится в записи TOC для этого поля SEQ.
# Само поле SEQ не будет отображать содержимое этой закладки.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Создайте закладку с содержимым, которое появится в записи TOC из‑за ссылки вышеуказанного поля SEQ на неё.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('SEQBookmark')
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', text from inside SEQBookmark.')
builder.end_bookmark('SEQBookmark')
builder.end_bookmark('TOCBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.Bookmark.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)


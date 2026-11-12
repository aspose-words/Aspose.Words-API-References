---
title: FieldToc.prefixed_sequence_identifier property
linktitle: prefixed_sequence_identifier property
articleTitle: prefixed_sequence_identifier property
second_title: Aspose.Words for Python
description: "FieldToc.prefixed_sequence_identifier property. Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number."
type: docs
weight: 120
url: /ru/python-net/aspose.words.fields/fieldtoc/prefixed_sequence_identifier/
---

## FieldToc.prefixed_sequence_identifier property

Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number.


```python
@property
def prefixed_sequence_identifier(self) -> str:
    ...

@prefixed_sequence_identifier.setter
def prefixed_sequence_identifier(self, value: str):
    ...

```

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

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)


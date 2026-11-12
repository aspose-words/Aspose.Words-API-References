---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fieldseq/bookmark_name/
---

## FieldSeq.bookmark_name property

Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

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

* module [aspose.words.fields](../../)
* class [FieldSeq](../)


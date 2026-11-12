---
title: FieldSeq.reset_number property
linktitle: reset_number property
articleTitle: reset_number property
second_title: Aspose.Words for Python
description: "FieldSeq.reset_number property. Gets or sets an integer number to reset the sequence number to"
type: docs
weight: 50
url: /ru/python-net/aspose.words.fields/fieldseq/reset_number/
---

## FieldSeq.reset_number property

Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent.


```python
@property
def reset_number(self) -> str:
    ...

@reset_number.setter
def reset_number(self, value: str):
    ...

```

### Examples

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

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)


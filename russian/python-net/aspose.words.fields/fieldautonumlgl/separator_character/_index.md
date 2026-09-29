---
title: FieldAutoNumLgl.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNumLgl.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 30
url: /ru/python-net/aspose.words.fields/fieldautonumlgl/separator_character/
---

## FieldAutoNumLgl.separator_character property

Gets or sets the separator character to be used.


```python
@property
def separator_character(self) -> str:
    ...

@separator_character.setter
def separator_character(self, value: str):
    ...

```

### Examples

Shows how to organize a document using AUTONUMLGL fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
filler_text = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + '\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '
# Поля AUTONUMLGL отображают номер, который увеличивается в каждом поле AUTONUMLGL внутри текущего уровня заголовка.
# Эти поля поддерживают отдельный счёт для каждого уровня заголовка,
# и каждое поле также отображает счёт полей AUTONUMLGL для всех уровней заголовков ниже своего.
# Изменение счётчика для любого уровня заголовка сбрасывает счётчики всех уровней выше этого уровня до 1.
# Это позволяет нам организовать наш документ в виде списка с оглавлением.
# Это первое поле AUTONUMLGL на уровне заголовка 1, отображающее в документе "1.".
ExField._insert_numbered_clause(builder, '\tHeading 1', filler_text, aw.StyleIdentifier.HEADING1)
# Это второе поле AUTONUMLGL на уровне заголовка 1, поэтому оно будет отображать "2.".
ExField._insert_numbered_clause(builder, '\tHeading 2', filler_text, aw.StyleIdentifier.HEADING1)
# Это первое поле AUTONUMLGL на уровне заголовка 2,
# и счётчик AUTONUMLGL для уровня заголовка ниже него равен "2", поэтому он будет отображать "2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 3', filler_text, aw.StyleIdentifier.HEADING2)
# Это первое поле AUTONUMLGL на уровне заголовка 3.
# Работая так же, как поле выше, оно будет отображать "2.1.1.".
ExField._insert_numbered_clause(builder, '\tHeading 4', filler_text, aw.StyleIdentifier.HEADING3)
# Это поле находится на уровне заголовка 2, и его соответствующий счётчик AUTONUMLGL равен 2, поэтому поле будет отображать "2.2.".
ExField._insert_numbered_clause(builder, '\tHeading 5', filler_text, aw.StyleIdentifier.HEADING2)
# Увеличение счётчика AUTONUMLGL для уровня заголовка ниже этого
# сбросило счётчик для этого уровня, поэтому это поле будет отображать "2.2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 6', filler_text, aw.StyleIdentifier.HEADING3)
for field in list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, list(doc.range.fields))):
    field = field.as_field_auto_num_lgl()
    # Символ-разделитель, который появляется в результате поля сразу после числа,
    # по умолчанию является точкой. Если мы оставим это свойство null,
    # наше последнее поле AUTONUMLGL будет отображать "2.2.1." в документе.
    self.assertIsNone(field.separator_character)
    # Установка пользовательского символа-разделителя и удаление конечной точки
    # изменит внешний вид этого поля с "2.2.1." на "2:2:1".
    # Мы применим это ко всем полям, которые мы создали.
    field.separator_character = ':'
    field.remove_trailing_period = True
    self.assertEqual(' AUTONUMLGL  \\s : \\e', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUMLGL.docx')
```

Shows how to organize a document using AUTONUMLGL fields (InsertNumberedClause).

```python
@staticmethod
def _insert_numbered_clause(builder, heading, contents, heading_style):
    builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, update_field=True)
    builder.current_paragraph.paragraph_format.style_identifier = heading_style
    builder.writeln(heading)
    # Этот текст будет принадлежать полю auto num legal выше него.
    # Он свернётся, когда мы щёлкнем по стрелке рядом с соответствующим полем AUTONUMLGL в Microsoft Word.
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNumLgl](../)


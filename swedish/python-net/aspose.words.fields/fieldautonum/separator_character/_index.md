---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldautonum/separator_character/
---

## FieldAutoNum.separator_character property

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

Shows how to number paragraphs using autonum fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Varje AUTONUM-fält visar det aktuella värdet av en löpande räknare för AUTONUM-fält,
# som låter oss automatiskt numrera objekt som en numrerad lista.
# Det här fältet kommer att visa siffran "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 1.')
self.assertEqual(' AUTONUM ', field.get_field_code())
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 2.')
# Separatortecknet, som visas i fältresultatet omedelbart efter siffran, är som standard en punkt.
# Om vi lämnar den här egenskapen null, kommer vårt andra AUTONUM-fält att visa "2." i dokumentet.
self.assertIsNone(field.separator_character)
# Vi kan sätta den här egenskapen så att det första tecknet i dess sträng används som det nya separatortecknet.
# I det här fallet kommer vårt AUTONUM-fält nu att visa "2:".
field.separator_character = ':'
self.assertEqual(' AUTONUM  \\s :', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)


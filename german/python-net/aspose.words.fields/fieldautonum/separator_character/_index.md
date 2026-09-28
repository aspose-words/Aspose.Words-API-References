---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldautonum/separator_character/
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
# Jedes AUTONUM-Feld zeigt den aktuellen Wert einer laufenden Zählung von AUTONUM-Feldern an,
# ermöglicht es uns, Elemente automatisch wie eine nummerierte Liste zu nummerieren.
# Dieses Feld zeigt die Zahl "1." an.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 1.')
self.assertEqual(' AUTONUM ', field.get_field_code())
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 2.')
# Das Trennzeichen, das im Feldresultat unmittelbar nach der Zahl erscheint, ist standardmäßig ein Punkt.
# Wenn wir diese Eigenschaft null lassen, zeigt unser zweites AUTONUM-Feld im Dokument "2." an.
self.assertIsNone(field.separator_character)
# Wir können diese Eigenschaft so festlegen, dass das erste Zeichen seiner Zeichenkette als neues Trennzeichen verwendet wird.
# In diesem Fall zeigt unser AUTONUM-Feld nun "2:" an.
field.separator_character = ':'
self.assertEqual(' AUTONUM  \\s :', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)


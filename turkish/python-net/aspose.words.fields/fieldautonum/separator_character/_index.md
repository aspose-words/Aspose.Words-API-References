---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldautonum/separator_character/
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
# Each AUTONUM field displays the current value of a running count of AUTONUM fields,
# bize otomatik olarak numaralı bir liste gibi öğeleri numaralandırma imkanı verir.
# Bu alan, "1." numarasını gösterecektir.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 1.')
self.assertEqual(' AUTONUM ', field.get_field_code())
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 2.')
# Ayırıcı karakter, sayının hemen ardından alan sonucunda görünen, varsayılan olarak bir nokta işaretidir.
# Bu özelliği null bırakırsak, ikinci AUTONUM alanımız belgede "2." gösterecektir.
self.assertIsNone(field.separator_character)
# Bu özelliği, dizisinin ilk karakterini yeni ayırıcı karakter olarak uygulamak için ayarlayabiliriz.
# Bu durumda, AUTONUM alanımız artık "2:" gösterecektir.
field.separator_character = ':'
self.assertEqual(' AUTONUM  \\s :', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)


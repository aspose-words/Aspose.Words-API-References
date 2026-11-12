---
title: FieldInclude.source_full_name property
linktitle: source_full_name property
articleTitle: source_full_name property
second_title: Aspose.Words for Python
description: "FieldInclude.source_full_name property. Gets or sets the location of the document."
type: docs
weight: 40
url: /tr/python-net/aspose.words.fields/fieldinclude/source_full_name/
---

## FieldInclude.source_full_name property

Gets or sets the location of the document.


```python
@property
def source_full_name(self) -> str:
    ...

@source_full_name.setter
def source_full_name(self, value: str):
    ...

```

### Examples

Shows how to create an INCLUDE field, and set its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Yerel dosya sistemindeki başka bir belgenin bir bölümünü içe aktarmak için bir INCLUDE alanı kullanabiliriz.
# Bu alanla referans verdiğimiz diğer belgeden yer imi, bu içe aktarılan bölümü içerir.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INCLUDE, update_field=True).as_field_include()
field.source_full_name = MY_DIR + 'Bookmarks.docx'
field.bookmark_name = 'MyBookmark1'
field.lock_fields = False
field.text_converter = 'Microsoft Word'
assert re.search(' INCLUDE .* MyBookmark1 \\\\\\\\c \\"Microsoft Word\\"', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INCLUDE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldInclude](../)


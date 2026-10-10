---
title: FieldOptions.default_document_author property
linktitle: default_document_author property
articleTitle: default_document_author property
second_title: Aspose.Words for Python
description: "FieldOptions.default_document_author property. Gets or sets default document author's name"
type: docs
weight: 70
url: /tr/python-net/aspose.words.fields/fieldoptions/default_document_author/
---

## FieldOptions.default_document_author property

Gets or sets default document author's name. If author's name is already specified in built-in document properties,
this option is not considered.


```python
@property
def default_document_author(self) -> str:
    ...

@default_document_author.setter
def default_document_author(self, value: str):
    ...

```

### Examples

Shows how to use an AUTHOR field to display a document creator's name.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# AUTHOR alanları, "Author" adlı yerleşik belge özelliğinden sonuçlarını alır.
# Microsoft Word'de bir belge oluşturup kaydedersek,
# bu özellikte kullanıcı adımız bulunacaktır.
# Ancak, Aspose.Words kullanarak programlı bir şekilde belge oluşturursak,
# "Author" özelliği, varsayılan olarak boş bir dize olacaktır.
self.assertEqual('', doc.built_in_document_properties.author)
# AUTHOR alanlarının kullanması için bir yedek yazar adı ayarlayın
# eğer "Author" özelliği boş bir dize içeriyorsa.
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# Bir değer içeren AUTHOR alanını güncellemek
# bu değeri "Author" yerleşik özelliğine uygulayacaktır.
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# Bu özelliği değiştirdikten sonra AUTHOR alanını güncellemek, bu değeri alana uygulayacaktır.
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# "Name" özelliğini değiştirdikten sonra bir AUTHOR alanını güncellerseniz,
# alan yeni adı gösterecek ve yeni adı yerleşik özelliğe uygulayacaktır.
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# AUTHOR alanları DefaultDocumentAuthor özelliğini etkilemez.
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)


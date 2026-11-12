---
title: SaveOptions.update_fields property
linktitle: update_fields property
articleTitle: update_fields property
second_title: Aspose.Words for Python
description: "SaveOptions.update_fields property. Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format"
type: docs
weight: 150
url: /tr/python-net/aspose.words.saving/saveoptions/update_fields/
---

## SaveOptions.update_fields property

Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format.
Default value for this property is ``True``.



```python
@property
def update_fields(self) -> bool:
    ...

@update_fields.setter
def update_fields(self, value: bool):
    ...

```

### Remarks

Allows to specify whether to mimic or not MS Word behavior.


### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# PAGE ve NUMPAGES alanlarıyla metin ekleyin. Bu alanlar gerçek zamanlı olarak doğru değeri göstermez.
# Bunları "Field.Update()" ve "Document.UpdateFields()" gibi güncelleme yöntemlerini kullanarak manuel olarak güncellememiz gerekecek.
# her seferinde doğru değerleri göstermeleri gerektiğinde.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
options = aw.saving.PdfSaveOptions()
# "UpdateFields" özelliğini "false" olarak ayarlayarak bir kaydetme işleminden hemen önce belgedeki tüm alanların güncellenmesini engelleyin.
# Bu, tüm alanlarımızın kaydetmeden önce güncel olacağını biliyorsak tercih edilen seçenektir.
# "UpdateFields" özelliğini "true" olarak ayarlayarak tüm belgeyi dolaşmak için
# alanlar ve PDF olarak kaydetmeden önce bunları güncelleyin. Bu, tüm alanların görüntülenmesini sağlayacak
# PDF içinde en doğru değerleri.
options.update_fields = update_fields
# PdfSaveOptions nesnelerini klonlayabiliriz.
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)


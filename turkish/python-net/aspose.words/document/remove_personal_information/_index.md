---
title: Document.remove_personal_information property
linktitle: remove_personal_information property
articleTitle: remove_personal_information property
second_title: Aspose.Words for Python
description: "Document.remove_personal_information property. Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document."
type: docs
weight: 370
url: /tr/python-net/aspose.words/document/remove_personal_information/
---

## Document.remove_personal_information property

Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and
document properties upon saving the document.


```python
@property
def remove_personal_information(self) -> bool:
    ...

@remove_personal_information.setter
def remove_personal_information(self, value: bool):
    ...

```

### Examples

Shows how to enable the removal of personal information during a manual save.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Kişisel bilgiler içeren bazı içerikler ekleyin.
doc.built_in_document_properties.author = 'John Doe'
doc.built_in_document_properties.company = 'Placeholder Inc.'
doc.start_track_revisions(author=doc.built_in_document_properties.author, date_time=datetime.datetime.now())
builder.write('Hello world!')
doc.stop_track_revisions()
# Bu bayrak, Dosya -> Seçenekler -> Güven Merkezi -> Güven Merkezi Ayarları... -> eşdeğerdir.
# Gizlilik Seçenekleri -> Microsoft Word'de "Kaydetme sırasında dosya özelliklerinden kişisel bilgileri kaldır"
doc.remove_personal_information = save_without_personal_info
# Bu seçenek, Aspose.Words kullanılarak yapılan bir kaydetme işlemi sırasında etkili olmayacaktır.
# Bayrak ayarlı olduğunda, Microsoft Word kullanarak belgeyi manuel olarak kaydettiğimizde kişisel veriler belgemizden kaldırılacaktır.
doc.save(file_name=ARTIFACTS_DIR + 'Document.RemovePersonalInformation.docx')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.RemovePersonalInformation.docx')
self.assertEqual(save_without_personal_info, doc.remove_personal_information)
self.assertEqual('John Doe', doc.built_in_document_properties.author)
self.assertEqual('Placeholder Inc.', doc.built_in_document_properties.company)
self.assertEqual('John Doe', doc.revisions[0].author)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)


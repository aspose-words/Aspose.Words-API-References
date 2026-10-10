---
title: Document.remove_personal_information property
linktitle: remove_personal_information property
articleTitle: remove_personal_information property
second_title: Aspose.Words for Python
description: "Document.remove_personal_information property. Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document."
type: docs
weight: 370
url: /zh/python-net/aspose.words/document/remove_personal_information/
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
# 插入包含个人信息的内容。
doc.built_in_document_properties.author = 'John Doe'
doc.built_in_document_properties.company = 'Placeholder Inc.'
doc.start_track_revisions(author=doc.built_in_document_properties.author, date_time=datetime.datetime.now())
builder.write('Hello world!')
doc.stop_track_revisions()
# 此标志等同于 File -> Options -> Trust Center -> Trust Center Settings... ->
# Privacy Options -> "Remove personal information from file properties on save" 在 Microsoft Word 中。
doc.remove_personal_information = save_without_personal_info
# 此选项在使用 Aspose.Words 进行保存操作时不会生效。
# 当我们使用 Microsoft Word 手动保存时，若设置了该标志，个人数据将从文档中被移除。
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


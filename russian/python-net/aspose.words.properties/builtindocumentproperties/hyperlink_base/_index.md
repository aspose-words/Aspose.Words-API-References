---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /ru/python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
---

## BuiltInDocumentProperties.hyperlink_base property

Specifies the base string used for evaluating relative hyperlinks in this document.


```python
@property
def hyperlink_base(self) -> str:
    ...

@hyperlink_base.setter
def hyperlink_base(self, value: str):
    ...

```

### Remarks

Aspose.Words does not use this property.




### Examples

Shows how to store the base part of a hyperlink in the document's properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте относительную гиперссылку на документ в локальной файловой системе с именем "Document.docx".
# Щелчок по ссылке в Microsoft Word откроет назначенный документ, если он доступен.
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# Эта ссылка относительная. Если в той же папке нет файла "Document.docx"
# как документ, содержащий эту ссылку, ссылка будет сломана.
self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'Document.docx'))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.BrokenLink.docx')
# Документ, к которому мы пытаемся создать ссылку, находится в другой директории, чем та, в которой мы планируем сохранить документ.
# Мы могли бы исправить такие ссылки, указав абсолютное имя файла в каждой из них.
# В качестве альтернативы мы могли бы задать базовую ссылку, к которой каждый гиперссылка с относительным именем файла
# будет добавлять перед своей ссылкой при щелчке.
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(system_helper.io.File.exist(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.WorkingLink.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)


---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /zh/python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
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
# 插入指向本地文件系统中名为 "Document.docx" 的文档的相对超链接。
# 在 Microsoft Word 中点击链接将打开指定的文档（如果该文档可用）。
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# 此链接是相对路径。如果同一文件夹中没有 "Document.docx"
# 作为包含此链接的文档，链接将会失效。
self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'Document.docx'))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.BrokenLink.docx')
# 我们尝试链接的文档位于与我们计划保存文档的目录不同的目录中。
# 我们可以通过在每个链接中使用绝对文件名来修复此类链接。
# 或者，我们可以提供一个基础链接，使每个带相对文件名的超链接
# 在点击时会在其链接前添加该基础链接。
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(system_helper.io.File.exist(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.WorkingLink.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)


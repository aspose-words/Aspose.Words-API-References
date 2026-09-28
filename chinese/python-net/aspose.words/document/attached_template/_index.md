---
title: Document.attached_template property
linktitle: attached_template property
articleTitle: attached_template property
second_title: Aspose.Words for Python
description: "Document.attached_template property. Gets or sets the full path of the template attached to the document."
type: docs
weight: 20
url: /zh/python-net/aspose.words/document/attached_template/
---

## Document.attached_template property

Gets or sets the full path of the template attached to the document.


```python
@property
def attached_template(self) -> str:
    ...

@attached_template.setter
def attached_template(self, value: str):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws if you attempt to set to a ``None`` value. |

### Remarks

Empty string means the document is attached to the Normal template.




### Examples

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# 启用自动样式更新，但不要附加模板文档。
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# 由于没有模板文档，文档没有地方跟踪样式更改。
# 使用 SaveOptions 对象自动设置模板
# 如果我们正在保存的文档没有模板的话。
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* property [BuiltInDocumentProperties.template](../../../aspose.words.properties/builtindocumentproperties/template/)


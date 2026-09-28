---
title: Document.automatically_update_styles property
linktitle: automatically_update_styles property
articleTitle: automatically_update_styles property
second_title: Aspose.Words for Python
description: "Document.automatically_update_styles property. Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word."
type: docs
weight: 30
url: /zh/python-net/aspose.words/document/automatically_update_styles/
---

## Document.automatically_update_styles property

Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the
attached template each time the document is opened in MS Word.


```python
@property
def automatically_update_styles(self) -> bool:
    ...

@automatically_update_styles.setter
def automatically_update_styles(self, value: bool):
    ...

```

### Examples

Shows how to attach a template to a document.

```python
doc = aw.Document()
# Microsoft Word 文档默认附带一个名为 "Normal.dotm" 的模板。
# 空白的 Aspose.Words 文档没有默认模板。
self.assertEqual('', doc.attached_template)
# 附加模板，然后设置标志以应用样式更改
# 在模板中将样式应用到我们文档的样式。
doc.attached_template = MY_DIR + 'Business brochure.dotx'
doc.automatically_update_styles = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.AutomaticallyUpdateStyles.docx')
```

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


---
title: Document.automatically_update_styles property
linktitle: automatically_update_styles property
articleTitle: automatically_update_styles property
second_title: Aspose.Words for Python
description: "Document.automatically_update_styles property. Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word."
type: docs
weight: 30
url: /tr/python-net/aspose.words/document/automatically_update_styles/
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
# Microsoft Word belgeleri varsayılan olarak "Normal.dotm" adlı bir ek şablonla birlikte gelir.
# Boş Aspose.Words belgeleri için varsayılan bir şablon yoktur.
self.assertEqual('', doc.attached_template)
# Bir şablon ekleyin, ardından stil değişikliklerini uygulamak için bayrağı ayarlayın
# şablon içinde belge stillerine.
doc.attached_template = MY_DIR + 'Business brochure.dotx'
doc.automatically_update_styles = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.AutomaticallyUpdateStyles.docx')
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Otomatik stil güncellemeyi etkinleştirin, ancak bir şablon belge eklemeyin.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Şablon belge olmadığı için, belge stil değişikliklerini izlemek için bir yeri yoktu.
# Bir SaveOptions nesnesi kullanarak otomatik olarak bir şablon ayarlayın
# eğer kaydettiğimiz belge bir şablona sahip değilse.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)


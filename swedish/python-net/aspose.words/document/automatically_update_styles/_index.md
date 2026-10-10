---
title: Document.automatically_update_styles property
linktitle: automatically_update_styles property
articleTitle: automatically_update_styles property
second_title: Aspose.Words for Python
description: "Document.automatically_update_styles property. Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word."
type: docs
weight: 30
url: /sv/python-net/aspose.words/document/automatically_update_styles/
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
# Microsoft Word-dokument har som standard en bifogad mall som heter "Normal.dotm".
# Det finns ingen standardmall för tomma Aspose.Words-dokument.
self.assertEqual('', doc.attached_template)
# Bifoga en mall och sätt sedan flaggan för att tillämpa stiländringar
# i mallen till stilar i vårt dokument.
doc.attached_template = MY_DIR + 'Business brochure.dotx'
doc.automatically_update_styles = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.AutomaticallyUpdateStyles.docx')
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Aktivera automatisk stiluppdatering, men bifoga inte ett mall-dokument.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Eftersom det inte finns något mall-dokument hade dokumentet ingen plats att spåra stiländringar.
# Använd ett SaveOptions-objekt för att automatiskt ange en mall
# om ett dokument som vi sparar inte har en.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)


---
title: Document.automatically_update_styles property
linktitle: automatically_update_styles property
articleTitle: automatically_update_styles property
second_title: Aspose.Words for Python
description: "Document.automatically_update_styles property. Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word."
type: docs
weight: 30
url: /ru/python-net/aspose.words/document/automatically_update_styles/
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
# Документы Microsoft Word по умолчанию поставляются с прикреплённым шаблоном под названием "Normal.dotm".
# Для пустых документов Aspose.Words нет шаблона по умолчанию.
self.assertEqual('', doc.attached_template)
# Прикрепите шаблон, затем установите флаг для применения изменений стилей
# внутри шаблона к стилям в нашем документе.
doc.attached_template = MY_DIR + 'Business brochure.dotx'
doc.automatically_update_styles = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.AutomaticallyUpdateStyles.docx')
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Включите автоматическое обновление стилей, но не прикрепляйте шаблонный документ.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Поскольку шаблонного документа нет, у документа не было места для отслеживания изменений стилей.
# Используйте объект SaveOptions для автоматической установки шаблона
# если сохраняемый документ не имеет его.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)


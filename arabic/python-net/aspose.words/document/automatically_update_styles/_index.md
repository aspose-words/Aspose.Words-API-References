---
title: Document.automatically_update_styles property
linktitle: automatically_update_styles property
articleTitle: automatically_update_styles property
second_title: Aspose.Words for Python
description: "Document.automatically_update_styles property. Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word."
type: docs
weight: 30
url: /ar/python-net/aspose.words/document/automatically_update_styles/
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
# مستندات Microsoft Word تأتي بشكل افتراضي مع قالب مرفق يُدعى "Normal.dotm".
# لا يوجد قالب افتراضي للمستندات الفارغة في Aspose.Words.
self.assertEqual('', doc.attached_template)
# قم بإرفاق قالب، ثم اضبط العلامة لتطبيق تغييرات النمط
# داخل القالب إلى الأنماط في مستندنا.
doc.attached_template = MY_DIR + 'Business brochure.dotx'
doc.automatically_update_styles = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.AutomaticallyUpdateStyles.docx')
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# فعّل تحديث الأنماط تلقائيًا، ولكن لا تقم بإرفاق مستند قالب.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# نظرًا لعدم وجود مستند قالب، لم يكن للمستند مكان لتتبع تغييرات النمط.
# استخدم كائن SaveOptions لتعيين قالب تلقائيًا
# إذا كان المستند الذي نقوم بحفظه لا يحتوي على واحد.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)


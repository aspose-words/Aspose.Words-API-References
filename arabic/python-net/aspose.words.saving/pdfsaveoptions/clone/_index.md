---
title: PdfSaveOptions.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Python
description: "PdfSaveOptions.clone method. Creates a deep clone of this object."
type: docs
weight: 390
url: /ar/python-net/aspose.words.saving/pdfsaveoptions/clone/
---

## clone() {#default}

Creates a deep clone of this object.


```python
def clone(self):
    ...
```

### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج النص باستخدام حقول PAGE و NUMPAGES. هذه الحقول لا تعرض القيمة الصحيحة في الوقت الفعلي.
# سنحتاج إلى تحديثها يدويًا باستخدام أساليب التحديث مثل "Field.Update()" و "Document.UpdateFields()"
# في كل مرة نحتاج فيها إلى عرض قيم دقيقة.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# عيّن الخاصية "UpdateFields" إلى "false" لعدم تحديث جميع الحقول في المستند قبل عملية الحفظ مباشرةً.
# هذا هو الخيار المفضَّل إذا كنا نعلم أن جميع حقولنا ستكون محدثة قبل الحفظ.
# عيّن الخاصية "UpdateFields" إلى "true" لتكرار عبر جميع المستند
# الحقول وتحديثها قبل أن نحفظه كملف PDF. سيضمن ذلك أن جميع الحقول ستعرض
# أدق القيم في ملف PDF.
options.update_fields = update_fields
# يمكننا استنساخ كائنات PdfSaveOptions.
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)


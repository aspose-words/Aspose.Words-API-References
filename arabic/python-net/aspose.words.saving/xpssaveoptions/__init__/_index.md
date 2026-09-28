---
title: XpsSaveOptions constructor
linktitle: XpsSaveOptions constructor
articleTitle: XpsSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.XpsSaveOptions constructor"
type: docs
weight: 10
url: /ar/python-net/aspose.words.saving/xpssaveoptions/__init__/
---

## XpsSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS) format.



```python
def __init__(self):
    ...
```

## XpsSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS) or [SaveFormat.OPEN_XPS](../../../aspose.words/saveformat/#OPEN_XPS) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## Examples

Shows how to save a document to the XPS format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# أنشئ كائن "XpsSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .XPS.
xps_options = aw.saving.XpsSaveOptions(aw.SaveFormat.XPS)
# عيّن الخاصية "UseBookFoldPrintingSettings" إلى "true" لترتيب المحتويات
# في ملف XPS الناتج بطريقة تساعدنا على استخدامه لإنشاء كتيب.
# اضبط الخاصية "UseBookFoldPrintingSettings" إلى "false" لتصوير ملف XPS بشكل طبيعي.
xps_options.use_book_fold_printing_settings = render_text_as_book_fold
# إذا كنا نقوم بعرض المستند ككتيب، يجب علينا ضبط "MultiplePages"
# خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
if render_text_as_book_fold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# بمجرد طباعة هذا المستند، يمكننا تحويله إلى كتيب عن طريق تجميع الصفحات
# لتخرج من الطابعة وتطوى في الوسط.
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.BookFold.xps', save_options=xps_options)
```

## See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)


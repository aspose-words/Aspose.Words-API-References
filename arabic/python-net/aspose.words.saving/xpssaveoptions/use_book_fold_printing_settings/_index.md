---
title: XpsSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 60
url: /ar/python-net/aspose.words.saving/xpssaveoptions/use_book_fold_printing_settings/
---

## XpsSaveOptions.use_book_fold_printing_settings property

Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout,
if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/).



```python
@property
def use_book_fold_printing_settings(self) -> bool:
    ...

@use_book_fold_printing_settings.setter
def use_book_fold_printing_settings(self, value: bool):
    ...

```

### Remarks

If this option is specified, [FixedPageSaveOptions.page_set](../../fixedpagesaveoptions/page_set/) is ignored when saving.
This behavior matches MS Word.
If book fold printing settings are not specified in page setup, this option will have no effect.





### Examples

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

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)


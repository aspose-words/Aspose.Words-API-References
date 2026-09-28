---
title: OutlineOptions.default_bookmarks_outline_level property
linktitle: default_bookmarks_outline_level property
articleTitle: default_bookmarks_outline_level property
second_title: Aspose.Words for Python
description: "OutlineOptions.default_bookmarks_outline_level property. Specifies the default level in the document outline at which to display Word bookmarks."
type: docs
weight: 50
url: /ar/python-net/aspose.words.saving/outlineoptions/default_bookmarks_outline_level/
---

## OutlineOptions.default_bookmarks_outline_level property

Specifies the default level in the document outline at which to display Word bookmarks.


```python
@property
def default_bookmarks_outline_level(self) -> int:
    ...

@default_bookmarks_outline_level.setter
def default_bookmarks_outline_level(self, value: int):
    ...

```

### Remarks

Individual bookmarks level could be specified using [OutlineOptions.bookmarks_outline_levels](../bookmarks_outline_levels/) property.

Specify 0 and Word bookmarks will not be displayed in the document outline.
Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows to process bookmarks in headers/footers in a document that we are rendering to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'Bookmarks in headers and footers.docx')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
save_options = aw.saving.PdfSaveOptions()
# قم بتعيين الخاصية "PageMode" إلى "PdfPageMode.UseOutlines" لعرض لوحة التنقل بالمخطط في ملف PDF الناتج.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# قم بتعيين الخاصية "DefaultBookmarksOutlineLevel" إلى "1" لعرض جميع
# الإشارات المرجعية في المستوى الأول من المخطط في ملف PDF الناتج.
save_options.outline_options.default_bookmarks_outline_level = 1
# قم بتعيين الخاصية "HeaderFooterBookmarksExportMode" إلى "HeaderFooterBookmarksExportMode.None" لـ
# عدم تصدير أي إشارات مرجعية داخل رؤوس/تذييلات الصفحات.
# قم بتعيين الخاصية "HeaderFooterBookmarksExportMode" إلى "HeaderFooterBookmarksExportMode.First" لـ
# تصدير الإشارات المرجعية فقط في رؤوس/تذييلات القسم الأول.
# قم بتعيين الخاصية "HeaderFooterBookmarksExportMode" إلى "HeaderFooterBookmarksExportMode.All" لـ
# تصدير الإشارات المرجعية الموجودة في جميع الرؤوس/التذييلات.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)


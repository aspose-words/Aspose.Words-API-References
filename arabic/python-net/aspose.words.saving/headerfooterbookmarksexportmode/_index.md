---
title: HeaderFooterBookmarksExportMode enumeration
linktitle: HeaderFooterBookmarksExportMode enumeration
articleTitle: HeaderFooterBookmarksExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HeaderFooterBookmarksExportMode enumeration. Specifies how bookmarks in headers/footers are exported."
type: docs
weight: 220
url: /ar/python-net/aspose.words.saving/headerfooterbookmarksexportmode/
---

## HeaderFooterBookmarksExportMode enumeration

Specifies how bookmarks in headers/footers are exported.


### Members

| Name | Description |
| --- | --- |
| NONE | Bookmarks in headers/footers are not exported. |
| FIRST | Only bookmark in first header/footer of the section is exported. |
| ALL | Bookmarks in all headers/footers are exported. |

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

* module [aspose.words.saving](../)


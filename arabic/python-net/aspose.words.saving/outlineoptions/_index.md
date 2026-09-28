---
title: OutlineOptions class
linktitle: OutlineOptions class
articleTitle: OutlineOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.OutlineOptions class. Allows to specify outline options"
type: docs
weight: 570
url: /ar/python-net/aspose.words.saving/outlineoptions/
---

## OutlineOptions class

Allows to specify outline options.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [OutlineOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmarks_outline_levels](./bookmarks_outline_levels/) | Allows to specify individual bookmarks outline level. |
| [create_missing_outline_levels](./create_missing_outline_levels/) | Gets or sets a value determining whether or not to create missing outline levels when the document is  exported. |
| [create_outlines_for_headings_in_tables](./create_outlines_for_headings_in_tables/) | Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables. |
| [default_bookmarks_outline_level](./default_bookmarks_outline_level/) | Specifies the default level in the document outline at which to display Word bookmarks. |
| [expanded_outline_levels](./expanded_outline_levels/) | Specifies how many levels in the document outline to show expanded when the file is viewed. |
| [headings_outline_levels](./headings_outline_levels/) | Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline. |

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


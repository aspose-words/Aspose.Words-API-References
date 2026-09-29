---
title: OutlineOptions.default_bookmarks_outline_level property
linktitle: default_bookmarks_outline_level property
articleTitle: default_bookmarks_outline_level property
second_title: Aspose.Words for Python
description: "OutlineOptions.default_bookmarks_outline_level property. Specifies the default level in the document outline at which to display Word bookmarks."
type: docs
weight: 50
url: /tr/python-net/aspose.words.saving/outlineoptions/default_bookmarks_outline_level/
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
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
save_options = aw.saving.PdfSaveOptions()
# \"PageMode\" özelliğini \"PdfPageMode.UseOutlines\" olarak ayarlayın, çıktı PDF'inde taslak gezinme panelini göstermek için.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# \"DefaultBookmarksOutlineLevel\" özelliğini \"1\" olarak ayarlayın, tüm
# yer imlerini çıktı PDF'inde taslağın ilk seviyesinde görüntülemek için.
save_options.outline_options.default_bookmarks_outline_level = 1
# \"HeaderFooterBookmarksExportMode\" özelliğini \"HeaderFooterBookmarksExportMode.None\" olarak ayarlayın,
# başlık/altbilgi içinde bulunan hiçbir yer imini dışa aktarmamak için.
# \"HeaderFooterBookmarksExportMode\" özelliğini \"HeaderFooterBookmarksExportMode.First\" olarak ayarlayın,
# yalnızca ilk bölümün başlık/altbilgilerindeki yer imlerini dışa aktarmak için.
# \"HeaderFooterBookmarksExportMode\" özelliğini \"HeaderFooterBookmarksExportMode.All\" olarak ayarlayın,
# tüm başlık/altbilgilerdeki yer imlerini dışa aktarmak için.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)


---
title: PdfSaveOptions.header_footer_bookmarks_export_mode property
linktitle: header_footer_bookmarks_export_mode property
articleTitle: header_footer_bookmarks_export_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.header_footer_bookmarks_export_mode property. Determines how bookmarks in headers/footers are exported."
type: docs
weight: 200
url: /tr/python-net/aspose.words.saving/pdfsaveoptions/header_footer_bookmarks_export_mode/
---

## PdfSaveOptions.header_footer_bookmarks_export_mode property

Determines how bookmarks in headers/footers are exported.


```python
@property
def header_footer_bookmarks_export_mode(self) -> aspose.words.saving.HeaderFooterBookmarksExportMode:
    ...

@header_footer_bookmarks_export_mode.setter
def header_footer_bookmarks_export_mode(self, value: aspose.words.saving.HeaderFooterBookmarksExportMode):
    ...

```

### Remarks

The default value is [HeaderFooterBookmarksExportMode.ALL](../../headerfooterbookmarksexportmode/#ALL).

This property is used in conjunction with the [PdfSaveOptions.outline_options](../outline_options/) option.




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
* class [PdfSaveOptions](../)


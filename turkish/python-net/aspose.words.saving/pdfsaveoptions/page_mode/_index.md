---
title: PdfSaveOptions.page_mode property
linktitle: page_mode property
articleTitle: page_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.page_mode property. Specifies how the PDF document should be displayed when opened in a PDF reader."
type: docs
weight: 280
url: /tr/python-net/aspose.words.saving/pdfsaveoptions/page_mode/
---

## PdfSaveOptions.page_mode property

Specifies how the PDF document should be displayed when opened in a PDF reader.


```python
@property
def page_mode(self) -> aspose.words.saving.PdfPageMode:
    ...

@page_mode.setter
def page_mode(self, value: aspose.words.saving.PdfPageMode):
    ...

```

### Remarks

The default value is [PdfPageMode.USE_OUTLINES](../../pdfpagemode/#USE_OUTLINES).



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


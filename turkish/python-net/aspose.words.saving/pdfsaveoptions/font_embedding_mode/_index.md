---
title: PdfSaveOptions.font_embedding_mode property
linktitle: font_embedding_mode property
articleTitle: font_embedding_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.font_embedding_mode property. Specifies the font embedding mode."
type: docs
weight: 180
url: /tr/python-net/aspose.words.saving/pdfsaveoptions/font_embedding_mode/
---

## PdfSaveOptions.font_embedding_mode property

Specifies the font embedding mode.


```python
@property
def font_embedding_mode(self) -> aspose.words.saving.PdfFontEmbeddingMode:
    ...

@font_embedding_mode.setter
def font_embedding_mode(self, value: aspose.words.saving.PdfFontEmbeddingMode):
    ...

```

### Remarks

The default value is [PdfFontEmbeddingMode.EMBED_ALL](../../pdffontembeddingmode/#EMBED_ALL).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains
non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded.
[PdfFontEmbeddingMode.EMBED_ALL](../../pdffontembeddingmode/#EMBED_ALL) value will be used automatically when saving to
PDF/A and PDF/UA.




### Examples

Shows how to set Aspose.Words to skip embedding Arial and Times New Roman fonts into a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# "Arial" standart bir yazı tipidir ve "Courier New" standart dışı bir yazı tipidir.
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
options = aw.saving.PdfSaveOptions()
# "EmbedFullFonts" özelliğini "true" olarak ayarlayarak çıkış PDF'inde gömülü tüm yazı tiplerinin her glifini gömün.
options.embed_full_fonts = True
# "FontEmbeddingMode" özelliğini "EmbedAll" olarak ayarlayarak çıkış PDF'inde tüm yazı tiplerini gömün.
# "FontEmbeddingMode" özelliğini "EmbedNonstandard" olarak ayarlayarak çıkış PDF'inde yalnızca standart dışı yazı tiplerinin gömülmesine izin verin.
# "FontEmbeddingMode" özelliğini "EmbedNone" olarak ayarlayarak çıkış PDF'inde hiçbir yazı tipi gömülmesin.
options.font_embedding_mode = pdf_font_embedding_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedWindowsFonts.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)


---
title: PdfSaveOptions.font_embedding_mode property
linktitle: font_embedding_mode property
articleTitle: font_embedding_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.font_embedding_mode property. Specifies the font embedding mode."
type: docs
weight: 180
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/font_embedding_mode/
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
# "Arial" 是标准字体，而 "Courier New" 是非标准字体。
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 将 "EmbedFullFonts" 属性设置为 "true"，以在输出的 PDF 中嵌入每个已嵌入字体的所有字形。
options.embed_full_fonts = True
# 将 "FontEmbeddingMode" 属性设置为 "EmbedAll"，以在输出的 PDF 中嵌入所有字体。
# 将 "FontEmbeddingMode" 属性设置为 "EmbedNonstandard"，仅允许在输出的 PDF 中嵌入非标准字体。
# 将 "FontEmbeddingMode" 属性设置为 "EmbedNone"，以在输出的 PDF 中不嵌入任何字体。
options.font_embedding_mode = pdf_font_embedding_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedWindowsFonts.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)


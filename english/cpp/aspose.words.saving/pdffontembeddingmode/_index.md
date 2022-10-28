---
title: PdfFontEmbeddingMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how Aspose.Words should embed fonts.
type: docs
weight: 950
url: /cpp/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enum


Specifies how Aspose.Words should embed fonts.

### Values

| Name | Value | Description |
| --- | --- | --- |
| EmbedAll | 0 | Aspose.Words embeds all fonts. |
| EmbedNonstandard | 1 | Aspose.Words embeds all fonts excepting standard Windows fonts Arial and Times New Roman. Only Arial and Times New Roman fonts are affected in this mode because MS Word doesn't embed only these fonts when saving document to PDF. |
| EmbedNone | 2 | Aspose.Words do not embed any fonts. |


## Examples




Shows how to set Aspose.Words to skip embedding Arial and Times New Roman fonts into a PDF document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// "Arial" is a standard font, and "Courier New" is a nonstandard font.
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "EmbedFullFonts" property to "true" to embed every glyph of every embedded font in the output PDF.
options->set_EmbedFullFonts(true);

// Set the "FontEmbeddingMode" property to "EmbedAll" to embed all fonts in the output PDF.
// Set the "FontEmbeddingMode" property to "EmbedNonstandard" to only allow nonstandard fonts' embedding in the output PDF.
// Set the "FontEmbeddingMode" property to "EmbedNone" to not embed any fonts in the output PDF.
options->set_FontEmbeddingMode(pdfFontEmbeddingMode);

doc->Save(ArtifactsDir + u"PdfSaveOptions.EmbedWindowsFonts.pdf", options);

switch (pdfFontEmbeddingMode)
{
case PdfFontEmbeddingMode::EmbedAll:
    ASSERT_LT(1000000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"PdfSaveOptions.EmbedWindowsFonts.pdf")->get_Length());
    break;

case PdfFontEmbeddingMode::EmbedNonstandard:
    ASSERT_LT(480000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"PdfSaveOptions.EmbedWindowsFonts.pdf")->get_Length());
    break;

case PdfFontEmbeddingMode::EmbedNone:
    ASSERT_GE(4217, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"PdfSaveOptions.EmbedWindowsFonts.pdf")->get_Length());
    break;
}
```


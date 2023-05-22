---
title: Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode method
linktitle: get_FontEmbeddingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode method. Specifies the font embedding mode in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_fontembeddingmode/
---
## PdfSaveOptions::get_FontEmbeddingMode method


Specifies the font embedding mode.

```cpp
Aspose::Words::Saving::PdfFontEmbeddingMode Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode() const
```

## Remarks


The default value is [EmbedAll](../../pdffontembeddingmode/).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. [EmbedAll](../../pdffontembeddingmode/) value will be used automatically when saving to PDF/A and PDF/UA.

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

## See Also

* Enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

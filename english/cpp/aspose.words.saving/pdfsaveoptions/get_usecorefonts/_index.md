---
title: get_UseCoreFonts
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts.
type: docs
weight: 404
url: /cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## Remarks


The default value is **false**. When this value is set to **true** Arial, Times New Roman, Courier New and Symbol fonts are replaced in PDF document with corresponding core Type 1 font.

Core PDF fonts, or their font metrics and suitable substitution fonts, are required to be available to any PDF viewer application.

This setting works only for the text in ANSI (Windows-1252) encoding. Non-ANSI text will be written with embedded TrueType font regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. **false** value will be used automatically when saving to PDF/A and PDF/UA.

Core fonts are not supported when saving to PDF 2.0 format. **false** value will be used automatically when saving to PDF 2.0.

This option has a higher priority then [FontEmbeddingMode](../get_fontembeddingmode/) option.

## Examples



Shows how enable/disable PDF Type 1 font substitution. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "UseCoreFonts" property to "true" to replace some fonts,
// including the two fonts in our document, with their PDF Type 1 equivalents.
// Set the "UseCoreFonts" property to "false" to not apply PDF Type 1 fonts.
options->set_UseCoreFonts(useCoreFonts);

doc->Save(ArtifactsDir + u"PdfSaveOptions.EmbedCoreFonts.pdf", options);

if (useCoreFonts)
{
    ASSERT_GE(3000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"PdfSaveOptions.EmbedCoreFonts.pdf")->get_Length());
}
else
{
    ASSERT_LT(30000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"PdfSaveOptions.EmbedCoreFonts.pdf")->get_Length());
}
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)

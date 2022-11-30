---
title: get_EmbedFullFonts
second_title: Aspose.Words for C++ API Reference
description: Controls how fonts are embedded into the resulting PDF documents.
type: docs
weight: 144
url: /cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


Controls how fonts are embedded into the resulting PDF documents.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## Remarks


The default value is **false**, which means the fonts are subsetted before embedding. Subsetting is useful if you want to keep the output file size smaller. Subsetting removes all unused glyphs from a font.

When this value is set to **true**, a complete font file is embedded into PDF without subsetting. This will result in larger output files, but can be a useful option when you want to edit the resulting PDF later (e.g. add more text).

Some fonts are large (several megabytes) and embedding them without subsetting will result in large output documents.

## Examples



Shows how to enable or disable subsetting when embedding fonts while rendering a document to PDF. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Configure our font sources to ensure that we have access to both the fonts in this document.
ArrayPtr<SharedPtr<FontSourceBase>> originalFontsSources = FontSettings::get_DefaultInstance()->GetFontsSources();
auto folderFontSource = MakeObject<FolderFontSource>(FontsDir, true);
FontSettings::get_DefaultInstance()->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({originalFontsSources[0], folderFontSource}));

ArrayPtr<SharedPtr<FontSourceBase>> fontSources = FontSettings::get_DefaultInstance()->GetFontsSources();
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arial"; }));
ASSERT_TRUE(fontSources[1]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arvo"; }));

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Since our document contains a custom font, embedding in the output document may be desirable.
// Set the "EmbedFullFonts" property to "true" to embed every glyph of every embedded font in the output PDF.
// The document's size may become very large, but we will have full use of all fonts if we edit the PDF.
// Set the "EmbedFullFonts" property to "false" to apply subsetting to fonts, saving only the glyphs
// that the document is using. The file will be considerably smaller,
// but we may need access to any custom fonts if we edit the document.
options->set_EmbedFullFonts(embedFullFonts);

doc->Save(ArtifactsDir + u"PdfSaveOptions.EmbedFullFonts.pdf", options);

if (embedFullFonts)
{
    ASSERT_LT(500000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"PdfSaveOptions.EmbedFullFonts.pdf")->get_Length());
}
else
{
    ASSERT_GE(25000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"PdfSaveOptions.EmbedFullFonts.pdf")->get_Length());
}

// Restore the original font sources.
FontSettings::get_DefaultInstance()->SetFontsSources(originalFontsSources);
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)

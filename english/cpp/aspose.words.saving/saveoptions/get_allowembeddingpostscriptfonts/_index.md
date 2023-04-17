---
title: Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts method
linktitle: get_AllowEmbeddingPostScriptFonts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts method. Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is false in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## Remarks


Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) of the [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) property is set to **true**.

## Examples



Shows how to save the document with PostScript font. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// Load the font with PostScript to use in the document.
auto otf = MakeObject<MemoryFontSource>(System::IO::File::ReadAllBytes(FontsDir + u"AllegroOpen.otf"));
doc->set_FontSettings(MakeObject<FontSettings>());
doc->get_FontSettings()->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({otf}));

// Embed TrueType fonts.
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// Allow embedding PostScript fonts while embedding TrueType fonts.
// Microsoft Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.
SharedPtr<SaveOptions> saveOptions = SaveOptions::CreateSaveOptions(SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(ArtifactsDir + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts metod"
linktitle: "get_AllowEmbeddingPostScriptFonts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts metod. Hämtar eller anger ett booleskt värde som indikerar om inbäddning av teckensnitt med PostScript‑konturer ska tillåtas när TrueType‑teckensnitt inbäddas i ett dokument vid sparande. Standardvärdet är false i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


Hämtar eller anger ett booleskt värde som indikerar om inbäddning av teckensnitt med PostScript‑konturer ska tillåtas när TrueType‑teckensnitt inbäddas i ett dokument när det sparas. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## Anmärkningar


Observera att Word inte inbäddar PostScript‑teckensnitt, men kan öppna dokument med inbäddade teckensnitt av denna typ.

Detta alternativ fungerar endast när [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) för [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) egenskapen är satt till **true**.

## Exempel



Visar hur man sparar dokumentet med PostScript-typsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// Läs in typsnittet med PostScript för att använda i dokumentet.
auto otf = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(System::IO::File::ReadAllBytes(get_FontsDir() + u"AllegroOpen.otf"));
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({otf}));

// Bädda in TrueType-typsnitt.
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// Tillåt inbäddning av PostScript-typsnitt samtidigt som TrueType-typsnitt bäddas in.
// Microsoft Word bäddar inte in PostScript-typsnitt, men kan öppna dokument med inbäddade typsnitt av den här typen.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(get_ArtifactsDir() + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## Se även

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

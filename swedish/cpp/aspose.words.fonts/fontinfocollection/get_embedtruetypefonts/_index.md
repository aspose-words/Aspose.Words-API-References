---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts‑metod"
linktitle: "get_EmbedTrueTypeFonts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts‑metod. Anger om TrueType‑teckensnitt ska bäddas in i ett dokument när det sparas. Standardvärdet för denna egenskap är false i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


Anger om TrueType-teckensnitt ska bäddas in i ett dokument när det sparas eller inte. Standardvärdet för denna egenskap är **false**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## Anmärkningar


Att bädda in TrueType‑teckensnitt gör att andra kan visa dokumentet med samma teckensnitt som användes för att skapa det, men kan avsevärt öka dokumentets storlek.

Detta alternativ fungerar endast för formaten DOC, DOCX och RTF.

## Exempel



Visar hur man sparar ett dokument med inbäddade TrueType-teckensnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Se även

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)

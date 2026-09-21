---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts‑metod"
linktitle: "get_EmbedSystemFonts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts‑metod. Anger om System‑teckensnitt ska bäddas in i dokumentet eller inte. Standardvärdet för denna egenskap är false. Detta alternativ fungerar endast när EmbedTrueTypeFonts‑alternativet är satt till true i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


Anger om System‑teckensnitt ska bäddas in i dokumentet eller inte. Standardvärdet för denna egenskap är **false**. Detta alternativ fungerar endast när [EmbedTrueTypeFonts](../get_embedtruetypefonts/)‑alternativet är satt till **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## Anmärkningar


Att sätta denna egenskap till **true** är användbart om användaren har ett östasiatiskt system och vill skapa ett dokument som är läsbart för andra som inte har teckensnitt för det språket på sitt system. Till exempel kan en användare på ett japanskt system välja att bädda in teckensnitten i ett dokument så att det japanska dokumentet blir läsbart på alla system.

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

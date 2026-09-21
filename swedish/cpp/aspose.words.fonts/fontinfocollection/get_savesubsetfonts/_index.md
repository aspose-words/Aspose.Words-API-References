---
title: "Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts metod"
linktitle: "get_SaveSubsetFonts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts method. Anger om en delmängd av de inbäddade TrueType-teckensnitten ska sparas med dokumentet eller inte. Standardvärdet för denna egenskap är false. Detta alternativ fungerar endast när egenskapen EmbedTrueTypeFonts är satt till true i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


Anger om en delmängd av de inbäddade TrueType-teckensnitten ska sparas med dokumentet eller inte. Standardvärdet för denna egenskap är **false**. Detta alternativ fungerar endast när [EmbedTrueTypeFonts](../get_embedtruetypefonts/) egenskapen är satt till **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


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

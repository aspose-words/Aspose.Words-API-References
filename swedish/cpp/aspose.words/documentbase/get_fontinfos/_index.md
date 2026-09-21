---
title: "Aspose::Words::DocumentBase::get_FontInfos metod"
linktitle: "get_FontInfos"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBase::get_FontInfos metod. Ger åtkomst till egenskaper för teckensnitt som används i detta dokument i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


Tillhandahåller åtkomst till egenskaper för teckensnitt som används i detta dokument.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## Anmärkningar


Denna samling av teckensnittdefinitioner läses in som den är från dokumentet. [Font](../../font/) definitioner kan vara valfria, saknas eller vara ofullständiga i vissa dokument.

Lita inte på denna samling för att fastställa att ett visst teckensnitt används i dokumentet. Du bör endast använda denna samling för att få information om teckensnitt som kan användas i dokumentet.

## Exempel



Visar hur man skriver ut detaljerna för vilka teckensnitt som finns i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Skriv ut alla använda och oanvända teckensnitt i dokumentet.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


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

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Fonts::FontInfoCollection class"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfoCollection class. Representerar en samling av teckensnitt som används i ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


Representerar en samling teckensnitt som används i ett dokument. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | Bestämmer om samlingen innehåller ett teckensnitt med det angivna namnet. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Hämtar antalet element som finns i samlingen. |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | Anger om System-teckensnitt ska bäddas in i dokumentet eller inte. Standardvärdet för denna egenskap är **false**. Detta alternativ fungerar endast när alternativet [EmbedTrueTypeFonts](./get_embedtruetypefonts/) är satt till **true**. |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | Anger om TrueType-teckensnitt ska bäddas in i ett dokument när det sparas eller inte. Standardvärdet för denna egenskap är **false**. |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | Anger om en delmängd av de inbäddade TrueType-teckensnitten ska sparas med dokumentet eller inte. Standardvärdet för denna egenskap är **false**. Detta alternativ fungerar endast när egenskapen [EmbedTrueTypeFonts](./get_embedtruetypefonts/) är satt till **true**. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt som kan användas för att iterera över alla objekt i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Hämtar ett teckensnitt med det angivna namnet. |
| [idx_get](./idx_get/)(int32_t) | Hämtar ett teckensnitt på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | Sättare för [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/). |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | Sättare för [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/). |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | Sättare för [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beskrivning |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Anmärkningar


Objekten är [FontInfo](../fontinfo/) objekt.

Du skapar inte instanser av denna klass direkt. Använd egenskapen [FontInfos](../../aspose.words/documentbase/get_fontinfos/) för att komma åt samlingen av teckensnitt som definieras i dokumentet.

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)

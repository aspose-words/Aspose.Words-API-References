---
title: "Aspose::Words::WarningInfoCollection-klass"
linktitle: "WarningInfoCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::WarningInfoCollection-klass. Representerar en typad samling av WarningInfo-objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 75000
url: /sv/cpp/aspose.words/warninginfocollection/
---
## WarningInfoCollection class


Representerar en typad samling av [WarningInfo](../warninginfo/) objekt. För att lära dig mer, besök dokumentationsartikeln [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfoCollection : public Aspose::Words::IWarningCallback,
                              public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::WarningInfo>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Tar bort alla element från samlingen. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Hämtar antalet element som finns i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt som kan användas för att iterera över alla objekt i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar ett objekt på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
| [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) override | Implementerar gränssnittet [IWarningCallback](../iwarningcallback/). Lägger till en varning i denna samling. |
| [WarningInfoCollection](./warninginfocollection/)() |  |
## Typedefs

| Typedef | Beskrivning |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Anmärkningar


Du kan använda detta samlingsobjekt som den enklaste formen av [IWarningCallback](../iwarningcallback/)‑implementation för att samla alla varningar som Aspose.Words genererar under en inläsnings‑ eller sparningsoperation. Skapa en instans av denna klass och tilldela den till egenskapen [WarningCallback](../../aspose.words.loading/loadoptions/get_warningcallback/) eller [WarningCallback](../documentbase/get_warningcallback/).

## Exempel



Visar hur man ställer in egenskapen för att hitta den närmaste matchen för ett saknat teckensnitt från de tillgängliga teckensnittskällorna.
```cpp
// Öppna ett dokument som innehåller text formaterad med ett teckensnitt som inte finns i någon av våra teckensnittskällor.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Tilldela en återuppringning för att hantera varningar om teckensnittssubstitution.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Ange ett standardteckensnittsnamn och aktivera teckensnittssubstitution.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Ursprungliga teckensnittsmått bör användas efter teckensnittssubstitution.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Vi får en varning om teckensnittssubstitution om vi sparar ett dokument med ett saknat teckensnitt.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## Se även

* Interface [IWarningCallback](../iwarningcallback/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

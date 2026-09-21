---
title: "Aspose::Words::WarningType-enum"
linktitle: "WarningType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::WarningType-enum. Anger typen av varning som utfärdas av Aspose.Words under inläsning eller sparande av dokument i C++."
type: docs
weight: 129000
url: /sv/cpp/aspose.words/warningtype/
---
## WarningType enum


Anger typen av varning som utfärdas av Aspose.Words under dokumentladdning eller -sparande.

```cpp
enum class WarningType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| DataLossCategory | 255 | Viss text/tecken/bild eller annan data kommer att saknas antingen i dokumentträdet efter inläsning eller i det skapade dokumentet efter sparning. |
| DataLoss | 1 | Generisk dataförlust, ingen specifik kod. |
| MajorFormattingLossCategory | 65280 | Det resulterande dokumentet eller en viss plats i det kan se väsentligt annorlunda ut jämfört med originaldokumentet. |
| MajorFormattingLoss | 256 | Generisk större formateringsförlust, ingen specifik kod. |
| MinorFormattingLossCategory | 16711680 | Det resulterande dokumentet eller en viss plats i det kan se något annorlunda ut jämfört med det ursprungliga dokumentet. |
| MinorFormattingLoss | 65536 | Generisk mindre formateringsförlust, ingen specifik kod. |
| FontSubstitution | 131072 | [Font](../font/) har ersatts. |
| FontEmbedding | 262144 | Förlust av inbäddad teckensnittsinformation vid dokumentlagring. |
| UnexpectedContentCategory | 251658240 | Viss innehåll i källdokumentet kunde inte identifieras (dvs. stöds inte), detta kan eller kan inte orsaka problem eller leda till data-/formateringsförlust. |
| UnexpectedContent | 16777216 | Generiskt oväntat innehåll, ingen specifik kod. |
| Hint | 268435456 | Råder om ett potentiellt problem eller föreslår en förbättring. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

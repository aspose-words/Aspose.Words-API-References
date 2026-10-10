---
title: "Aspose::Words::Fonts::FontInfoSubstitutionRule klass"
linktitle: "FontInfoSubstitutionRule"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfoSubstitutionRule klass. Regel för teckensnittsinformationssubstitution. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class


[Font](../../aspose.words/font/) info substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontInfoSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Anger om regeln är aktiverad eller inte. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Sättare för [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)

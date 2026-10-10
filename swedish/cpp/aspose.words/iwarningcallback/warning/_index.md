---
title: "Aspose::Words::IWarningCallback::Warning metod"
linktitle: "Varning"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IWarningCallback::Warning metod. Aspose.Words anropar denna metod när den stöter på ett problem under dokumentladdning eller -sparande som kan leda till förlust av formatering eller dataintegritet i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/iwarningcallback/warning/
---
## IWarningCallback::Warning method


Aspose.Words anropar den här metoden när den stöter på ett problem under dokumentladdning eller -sparande som kan leda till förlust av formatering eller datanoggrannhet.

```cpp
virtual void Aspose::Words::IWarningCallback::Warning(System::SharedPtr<Aspose::Words::WarningInfo> info)=0
```


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

* Class [WarningInfo](../../warninginfo/)
* Interface [IWarningCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

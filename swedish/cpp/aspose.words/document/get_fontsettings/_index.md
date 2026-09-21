---
title: "Aspose::Words::Document::get_FontSettings metod"
linktitle: "get_FontSettings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_FontSettings metod. Hämtar eller anger dokumentets teckensnittsinställningar i C++."
type: docs
weight: 25000
url: /sv/cpp/aspose.words/document/get_fontsettings/
---
## Document::get_FontSettings method


Hämtar eller anger dokumentets teckensnittinställningar.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Document::get_FontSettings() const
```

## Anmärkningar


Denna egenskap tillåter att ange teckensnittsinställningar per dokument. Om den är satt till **null** kommer standard-statisk teckensnittsinställning [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) att användas.

Standardvärdet är **null**.

## Exempel



Visar hur man ställer in typsnittsersättningsregler.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Standardtypsnittskällorna innehåller det första typsnittet som dokumentet använder.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Det andra typsnittet, \"Amethysta\", är otillgängligt.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Vi kan konfigurera en typsnittsersättningstabell som bestämmer
// vilka typsnitt Aspose.Words kommer att använda som ersättare för otillgängliga typsnitt.
// Ställ in två ersättningstypsnitt för \"Amethysta\": \"Arvo\" och \"Courier New\".
// Om den första ersättaren är otillgänglig försöker Aspose.Words använda den andra ersättaren, och så vidare.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// \"Amethysta\" är otillgängligt, och ersättningsregeln anger att det första typsnittet att använda som ersättning är \"Arvo\".
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// \"Arvo\" är också otillgängligt, men \"Courier New\" är det.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Utdokumentet kommer att visa texten som använder \"Amethysta\"-typsnittet formaterat med \"Courier New\".
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```

## Se även

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

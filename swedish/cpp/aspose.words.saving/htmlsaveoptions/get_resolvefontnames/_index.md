---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames metod"
linktitle: "get_ResolveFontNames"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames metod. Anger om teckensnittsfamiljenamn som används i dokumentet ska lösas upp och ersättas enligt FontSettings när de skrivs till HTML-baserade format i C++."
type: docs
weight: 42000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


Anger om teckensnittsfamiljenamn som används i dokumentet ska lösas upp och ersättas enligt [FontSettings](../../../aspose.words/document/get_fontsettings/) när de skrivs till HTML-baserade format.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## Anmärkningar


Som standard är detta alternativ inställt på **false** och teckensnittsfamiljenamn skrivs till HTML enligt vad som anges i källdokumenten. Det vill säga, [FontSettings](../../../aspose.words/document/get_fontsettings/) ignoreras och ingen upplösning eller ersättning av teckensnittsfamiljenamn utförs.

Om detta alternativ är inställt på **true**, använder Aspose.Words [FontSettings](../../../aspose.words/document/get_fontsettings/) för att lösa upp varje teckensnittsfamiljenamn som anges i ett källdokument till namnet på en tillgänglig teckensnittsfamilj, och utför teckensnittsersättning vid behov.

## Exempel



Visar hur man löser upp alla teckensnittsnamn innan de skrivs till HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Detta dokument innehåller text som nämner ett teckensnitt som vi inte har.
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// Om vi inte har något sätt att skaffa detta teckensnitt, och vi vill kunna visa all text
// i detta dokument i en utdata-HTML, kan vi ersätta det med ett annat teckensnitt.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// Som standard är detta alternativ inställt på 'False' och Aspose.Words skriver teckensnittsnamn enligt vad som anges i källdokumentet
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

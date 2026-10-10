---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation metod"
linktitle: "get_ExportLanguageInformation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation metod. Anger om språkinformation exporteras till HTML, MHTML eller EPUB. Standard är false i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


Anger om språkinformation exporteras till HTML, MHTML eller EPUB. Standard är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## Anmärkningar


När denna egenskap är inställd på **true** skriver Aspose.Words ut **lang**-HTML-attributet på dokumentelementen som specificerar språk. Detta kan behövas för att bevara språkrelaterad semantik.

## Exempel



Visar hur man bevarar språkinformation när man sparar till .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Använd byggaren för att skriva text medan du formaterar den i olika språkregioner.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// När dokumentet sparas till HTML kan vi skicka ett SaveOptions‑objekt
// för att antingen bevara eller förkasta varje formaterad texts språkregion.
// Om vi sätter flaggan "ExportLanguageInformation" till "true",
// kommer den genererade HTML-dokumentet att innehålla språkregionerna i "lang"-attributen på <span>-taggar.
// Om vi sätter flaggan "ExportLanguageInformation" till "false',
// kommer texten i det genererade HTML-dokumentet inte att innehålla någon språkregionsinformation.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportLanguageInformation(exportLanguageInformation);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"en-GB\">Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Привет, мир!</span>"));
}
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional‑metod"
linktitle: "get_ExportXhtmlTransitional"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional‑metoden. Anger om DOCTYPE‑deklarationen ska skrivas när du sparar till HTML eller MHTML. När true skrivs en DOCTYPE‑deklaration i dokumentet före rot‑elementet. Standardvärdet är false. Vid sparande till EPUB eller HTML5 (Html5) skrivs DOCTYPE‑deklarationen alltid i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportxhtmltransitional/
---
## HtmlSaveOptions::get_ExportXhtmlTransitional method


Anger om DOCTYPE‑deklarationen ska skrivas när du sparar till HTML eller MHTML. När **true** skrivs en DOCTYPE‑deklaration i dokumentet före rot‑elementet. Standardvärdet är **false**. Vid sparande till EPUB eller HTML5 ([Html5](../../htmlversion/)) skrivs DOCTYPE‑deklarationen alltid.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional() const
```

## Anmärkningar


Aspose.Words skriver alltid välformad HTML oavsett denna inställning.

När **true** kommer början av HTML‑utdatafilen att se ut så här:


```cpp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
             <!DOCTYPE html
                   PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
             "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
             <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```


Aspose.Words strävar efter att producera XHTML enligt specifikationen XHTML 1.0 Transitional, men resultatet validerar inte alltid mot DTD‑en. Vissa strukturer i ett Microsoft Word‑dokument är svåra eller omöjliga att översätta till ett dokument som validerar mot XHTML‑schemat. Till exempel tillåter inte XHTML nästlade listor (UL får inte vara nästlad i ett annat UL‑element), men i Microsoft Word‑dokument förekommer flernivålistor ofta.

## Exempel



Visar hur man visar en DOCTYPE-rubrik när man konverterar dokument till Xhtml 1.0 transitional-standarden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Vårt dokument kommer endast att innehålla en DOCTYPE-deklarationsrubrik om vi har satt flaggan "ExportXhtmlTransitional" till "true".
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html");
System::String newLine = System::Environment::get_NewLine();

if (showDoctypeDeclaration)
{
    ASSERT_TRUE(outDocContents.Contains(System::String::Format(u"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{0}", newLine) + System::String::Format(u"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{0}", newLine) + u"<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<html>"));
}
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation Methode"
linktitle: "get_ExportLanguageInformation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation Methode. Gibt an, ob Sprachinformationen nach HTML, MHTML oder EPUB exportiert werden. Standard ist false in C++."
type: docs
weight: 20000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


Gibt an, ob Sprachinformationen nach HTML, MHTML oder EPUB exportiert werden. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## Hinweise


Wenn diese Eigenschaft auf **true** gesetzt ist, gibt Aspose.Words das HTML-Attribut **lang** an den Dokumentelementen aus, die die Sprache angeben. Dies kann erforderlich sein, um sprachbezogene Semantik zu erhalten.

## Beispiele



Zeigt, wie man Sprachinformationen beim Speichern nach .html erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Verwenden Sie den Builder, um Text zu schreiben und ihn in verschiedenen Gebietsschemas zu formatieren.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// Beim Speichern des Dokuments als HTML können wir ein SaveOptions‑Objekt übergeben
// um entweder das Gebietsschema jedes formatierten Textes zu erhalten oder zu verwerfen.
// Wenn wir das Flag "ExportLanguageInformation" auf "true" setzen,
// Das Ausgabedokument HTML enthält die Gebietsschemas in den "lang"-Attributen von <span>-Tags.
// Wenn wir das Flag "ExportLanguageInformation" auf "false" setzen,
// Der Text im Ausgabedokument HTML wird keine Gebietsschema-Informationen enthalten.
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

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

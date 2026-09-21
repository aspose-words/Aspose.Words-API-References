---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText‑metod"
linktitle: "get_ExportDropDownFormFieldAsText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText‑metod. Styr hur rullgardinsformulärfält sparas till HTML eller MHTML. Standardvärdet är false i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


Styr hur rullgardinsformulärfält sparas till HTML eller MHTML. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## Anmärkningar


När den är inställd på **true** exporteras rullgardinsformulärfält som vanlig text. När den är **false** exporteras rullgardinsformulärfält som SELECT‑element i HTML.

Vid export till EPUB sparas text‑rullgardinsformulärfält alltid som text på grund av formatets krav.

## Exempel



Visar hur man får rullgardins‑kombinationsruta‑formulärfält att smälta in i stycke‑texten vid sparande till HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Använd en dokumentbyggare för att infoga en kombinationsruta med värdet "Two" markerat.
builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"One", u"Two", u"Three"}), 1);

// Flaggan "ExportDropDownFormFieldAsText" för detta SaveOptions‑objekt låter oss
// styra hur sparandet av dokumentet till HTML hanterar rullgardins‑kombinationsrutor.
// Att sätta den till "true" kommer att konvertera varje kombinationsruta till enkel text
// som visar kombinationsrutans för närvarande valda värde, vilket i praktiken fryser den.
// Att sätta den till "false" kommer att bevara kombinationsrutans funktionalitet med <select>- och <option>-taggar.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Two</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<select name=\"MyComboBox\">") + u"<option>One</option>" + u"<option selected=\"selected\">Two</option>" + u"<option>Three</option>" + u"</select>"));
}
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

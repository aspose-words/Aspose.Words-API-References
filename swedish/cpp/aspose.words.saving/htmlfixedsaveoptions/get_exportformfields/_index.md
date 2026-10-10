---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields‑metod"
linktitle: "get_ExportFormFields"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields‑metod. Hämtar eller anger om formulärfält exporteras som interaktiva objekt (som ''input''‑tagg) snarare än att konverteras till text eller grafik i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


Hämtar eller anger indikation på om formulärfält exporteras som interaktiva objekt (som 'input'-tagg) snarare än att konverteras till text eller grafik.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## Exempel



Visar hur man exporterar formulärfält till HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// När vi exporterar ett dokument med formulärfält till .html,
// finns det två sätt som Aspose.Words kan exportera formulärfält på.
// Om flaggan "ExportFormFields" sätts till "true" exporteras de som interaktiva objekt.
// Om flaggan sätts till "false" visas formulärfälten som vanlig text.
// Detta kommer att låsa dem på deras nuvarande värde och förhindra läsaren av vårt HTML‑dokument
// från att kunna interagera med dem.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportFormFields(exportFormFields);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")->get_Success());
}
```

## Se även

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

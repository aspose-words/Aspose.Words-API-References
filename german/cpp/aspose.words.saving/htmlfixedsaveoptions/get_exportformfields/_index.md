---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields Methode"
linktitle: "get_ExportFormFields"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields Methode. Gibt an oder legt fest, ob Formularfelder als interaktive Elemente (als ''input''‑Tag) exportiert werden, anstatt in Text oder Grafiken umgewandelt zu werden, in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


Liest oder legt die Angabe fest, ob Formularfelder als interaktive Elemente (als 'input'-Tag) exportiert werden, anstatt in Text oder Grafiken konvertiert zu werden.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## Beispiele



Zeigt, wie Formularfelder nach Html exportiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// Wenn wir ein Dokument mit Formularfeldern nach .html exportieren,
// gibt es zwei Möglichkeiten, wie Aspose.Words Formularfelder exportieren kann.
// Das Setzen des Flags "ExportFormFields" auf "true" exportiert sie als interaktive Objekte.
// Das Setzen dieses Flags auf "false" zeigt Formularfelder als Klartext an.
// Damit werden sie bei ihrem aktuellen Wert eingefroren und verhindern, dass der Leser unseres HTML‑Dokuments
// mit ihnen interagieren kann.
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

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

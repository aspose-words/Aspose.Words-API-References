---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers Methode"
linktitle: "get_ExportTocPageNumbers"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers Methode. Gibt an, ob Seitenzahlen in das Inhaltsverzeichnis geschrieben werden sollen, wenn HTML, MHTML und EPUB gespeichert werden. Der Standardwert ist false in C++."
type: docs
weight: 29000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


Gibt an, ob Seitenzahlen ins Inhaltsverzeichnis geschrieben werden sollen, wenn HTML, MHTML und EPUB gespeichert werden. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## Beispiele



Zeigt, wie Seitenzahlen angezeigt werden, wenn ein Dokument mit einem Inhaltsverzeichnis als .html gespeichert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Inhaltsverzeichnis ein und füllen Sie das Dokument anschließend mit Absätzen, die mit einer "Überschrift" formatiert sind.
// Stil, den das Inhaltsverzeichnis als Einträge übernimmt. Jeder Eintrag zeigt den Überschrifts‑Absatz links an,
// und die Seitenzahl, die die Überschrift rechts enthält.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 1");
builder->Writeln(u"Entry 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 3");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 4");
fieldToc->UpdatePageNumbers();
doc->UpdateFields();

// HTML‑Dokumente haben keine Seiten. Wenn wir dieses Dokument als HTML speichern,
// haben die Seitenzahlen, die unser Inhaltsverzeichnis anzeigt, keine Bedeutung.
// Wenn wir das Dokument als HTML speichern, können wir ein SaveOptions‑Objekt übergeben, um diese Seitenzahlen aus dem Inhaltsverzeichnis zu entfernen.
// Wenn wir das Flag "ExportTocPageNumbers" auf "true" setzen,
// zeigt jeder Inhaltsverzeichnis‑Eintrag die Überschrift, das Trennzeichen und die Seitenzahl an und bewahrt damit das Aussehen in Microsoft Word.
// Wenn wir das Flag "ExportTocPageNumbers" auf "false" setzen,
// wird der Speichervorgang sowohl das Trennzeichen als auch die Seitenzahl weglassen und die Überschrift für jeden Eintrag unverändert lassen.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportTocPageNumbers(exportTocPageNumbers);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Entry 1</span>") + u"<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " + u"-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" + u"<span>2</span>" + u"</p>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 2</span>" + u"</p>"));
}
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

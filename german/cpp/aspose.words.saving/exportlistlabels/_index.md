---
title: "Aspose::Words::Saving::ExportListLabels enum"
linktitle: "ExportListLabels"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ExportListLabels enum. Gibt an, wie Listenelemente zu HTML, MHTML und EPUB in C++ exportiert werden."
type: docs
weight: 56000
url: /de/cpp/aspose.words.saving/exportlistlabels/
---
## ExportListLabels enum


Gibt an, wie Listenelemente nach HTML, MHTML und EPUB exportiert werden.

```cpp
enum class ExportListLabels
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | 0 | Gibt Listenelemente im automatischen Modus aus. Verwendet HTML‑native Elemente, wenn möglich. |
| AsInlineText | 1 | Gibt alle Listenelemente als Inline‑Text aus. |
| ByHtmlTags | 2 | Gibt alle Listenelemente als HTML‑native Elemente aus. |


## Beispiele



Zeigt, wie das Exportieren von Listen nach HTML konfiguriert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
builder->get_ListFormat()->set_List(list);

builder->Writeln(u"Default numbered list item 1.");
builder->Writeln(u"Default numbered list item 2.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Default numbered list item 3.");
builder->get_ListFormat()->RemoveNumbers();

list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::OutlineHeadingsLegal);
builder->get_ListFormat()->set_List(list);

builder->Writeln(u"Outline legal heading list item 1.");
builder->Writeln(u"Outline legal heading list item 2.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Outline legal heading list item 3.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Outline legal heading list item 4.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Outline legal heading list item 5.");
builder->get_ListFormat()->RemoveNumbers();

// Beim Speichern des Dokuments als HTML können wir ein SaveOptions‑Objekt übergeben
// um zu entscheiden, welche HTML‑Elemente das Dokument zur Darstellung von Listen verwendet.
// Setzen der Eigenschaft "ExportListLabels" auf "ExportListLabels.AsInlineText"
// erstellt Listen, indem Spans formatiert werden.
// Setzen der Eigenschaft "ExportListLabels" auf "ExportListLabels.Auto" verwendet das <p>-Tag
// um Listen zu erstellen, wenn die Verwendung der <ol>- und <li>-Tags zu einem Verlust der Formatierung führen kann.
// Setzen der Eigenschaft "ExportListLabels" auf "ExportListLabels.ByHtmlTags"
// verwendet <ol>- und <li>-Tags, um alle Listen zu erstellen.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportListLabels(exportListLabels);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.List.html", options);
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.List.html");

switch (exportListLabels)
{
    case Aspose::Words::Saving::ExportListLabels::AsInlineText:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-left:72pt; margin-bottom:0pt; text-indent:-18pt; -aw-import:list-item; -aw-list-level-number:1; -aw-list-number-format:'%1.'; -aw-list-number-styles:'lowerLetter'; -aw-list-number-values:'1'; -aw-list-padding-sml:9.67pt\">") + u"<span style=\"-aw-import:ignore\">" + u"<span>a.</span>" + u"<span style=\"width:9.67pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" + u"</span>" + u"<span>Default numbered list item 3.</span>" + u"</p>"));
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; -aw-list-number-format:'%0.%1.%2.%3'; -aw-list-number-styles:'decimal decimal decimal decimal'; -aw-list-number-values:'2 1 1 1'; -aw-list-padding-sml:10.2pt\">") + u"<span style=\"-aw-import:ignore\">" + u"<span>2.1.1.1</span>" + u"<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" + u"</span>" + u"<span>Outline legal heading list item 5.</span>" + u"</p>"));
        break;

    case Aspose::Words::Saving::ExportListLabels::Auto:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">") + u"<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" + u"<span>Default numbered list item 3.</span>" + u"</li>" + u"</ol>"));
        break;

    case Aspose::Words::Saving::ExportListLabels::ByHtmlTags:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">") + u"<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" + u"<span>Default numbered list item 3.</span>" + u"</li>" + u"</ol>"));
        break;

}
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)

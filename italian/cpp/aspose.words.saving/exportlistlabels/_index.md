---
title: "Aspose::Words::Saving::ExportListLabels enum"
linktitle: "ExportListLabels"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ExportListLabels enum. Specifica come le etichette di elenco vengono esportate in HTML, MHTML ed EPUB in C++."
type: docs
weight: 56000
url: /it/cpp/aspose.words.saving/exportlistlabels/
---
## ExportListLabels enum


Specifica come le etichette delle liste vengono esportate in HTML, MHTML e EPUB.

```cpp
enum class ExportListLabels
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | 0 | Emette le etichette di elenco in modalità automatica. Usa gli elementi nativi HTML quando possibile. |
| AsInlineText | 1 | Emette tutte le etichette di elenco come testo in linea. |
| ByHtmlTags | 2 | Emette tutte le etichette di elenco come elementi nativi HTML. |


## Esempi



Mostra come configurare l'esportazione di elenchi in HTML.
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

// Quando si salva il documento in HTML, possiamo passare un oggetto SaveOptions
// per decidere quali elementi HTML il documento utilizzerà per rappresentare gli elenchi.
// Impostando la proprietà "ExportListLabels" su "ExportListLabels.AsInlineText"
// creerà elenchi formattando gli span.
// Impostare la proprietà "ExportListLabels" su "ExportListLabels.Auto" utilizzerà il tag <p>
// per creare elenchi nei casi in cui l'uso dei tag <ol> e <li> potrebbe causare perdita di formattazione.
// Impostare la proprietà "ExportListLabels" su "ExportListLabels.ByHtmlTags"
// utilizzerà i tag <ol> e <li> per creare tutti gli elenchi.
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

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)

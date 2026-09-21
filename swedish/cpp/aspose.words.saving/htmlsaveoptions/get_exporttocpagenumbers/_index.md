---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers metod"
linktitle: "get_ExportTocPageNumbers"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers metod. Anger om sidnummer ska skrivas till innehållsförteckning vid sparande av HTML, MHTML och EPUB. Standardvärdet är falskt i C++."
type: docs
weight: 29000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


Anger om sidnummer ska skrivas till innehållsförteckning när man sparar HTML, MHTML och EPUB. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## Exempel



Visar hur man visar sidnummer när man sparar ett dokument med en innehållsförteckning till .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en innehållsförteckning och fyll sedan i dokumentet med stycken formaterade med ett "Heading"
// stil som innehållsförteckningen kommer att plocka upp som poster. Varje post kommer att visa rubrikstycket till vänster,
// och sidnumret som innehåller rubriken till höger.
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

// HTML-dokument har inga sidor. Om vi sparar detta dokument som HTML,
// kommer sidnumren som vår innehållsförteckning visar att sakna mening.
// När vi sparar dokumentet som HTML kan vi skicka ett SaveOptions-objekt för att utelämna dessa sidnummer från innehållsförteckningen.
// Om vi sätter flaggan "ExportTocPageNumbers" till "true",
// kommer varje post i innehållsförteckningen att visa rubriken, separatorn och sidnumret, vilket bevarar dess utseende i Microsoft Word.
// Om vi sätter flaggan "ExportTocPageNumbers" till "false",
// kommer sparoperationen att utelämna både separatorn och sidnumret och låta rubriken för varje post förbli intakt.
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

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum. Anger hur Aspose.Words exporterar elementens bredd och höjd till HTML, MHTML och EPUB i C++."
type: docs
weight: 58000
url: /sv/cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


Anger hur Aspose.Words exporterar elementens bredd och höjd till HTML, MHTML och EPUB.

```cpp
enum class HtmlElementSizeOutputMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Alla | 0 | Alla elementstorlekar, både i absoluta och relativa enheter, som anges i dokumentet exporteras. |
| RelativeOnly | 1 | Elementstorlekar exporteras endast om de anges i relativa enheter i dokumentet. Fasta storlekar exporteras inte i detta läge. Visuella agenter beräknar saknade storlekar för att göra dokumentlayouten mer naturlig. |
| None | 2 | Elementstorlekar exporteras inte. Visuella agenter bygger layout automatiskt enligt relationen mellan elementen. |


## Exempel



Visar hur man bevarar negativa indrag i den exporterade .html‑filen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en tabell med ett negativt indrag, vilket kommer att skjuta den åt vänster förbi sidans vänstra gräns.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// Infoga en tabell med ett positivt indrag, vilket kommer att skjuta tabellen åt höger.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// När vi sparar ett dokument till HTML, kommer Aspose.Words endast att bevara negativa indrag
// såsom den vi har tillämpat på den första tabellen om vi sätter flaggan "AllowNegativeIndent"
// i ett SaveOptions‑objekt som vi kommer att skicka till "true".
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)

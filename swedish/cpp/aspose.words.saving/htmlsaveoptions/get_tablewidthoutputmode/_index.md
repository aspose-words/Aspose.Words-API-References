---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode‑metod"
linktitle: "get_TableWidthOutputMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode‑metod. Styr hur tabell-, rad- och cellbredder exporteras till HTML, MHTML eller EPUB. Standardvärdet är All i C++."
type: docs
weight: 47000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


Styr hur tabell-, rad- och cellbredder exporteras till HTML, MHTML eller EPUB. Standardvärdet är [All](../../htmlelementsizeoutputmode/).

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## Anmärkningar


I HTML‑formatet kan tabell-, rad- och cellelement (**%<table>**, **%<tr>**, **%<th>**, **%<td>**) ha sina bredder angivna antingen i relativa (procent) eller i absoluta enheter. I ett dokument i Aspose.Words kan tabeller, rader och celler också ha sina bredder angivna med antingen relativa eller absoluta enheter också.

När du konverterar ett dokument till HTML med Aspose.Words kan du vilja kontrollera hur tabell-, rad- och cellbredder exporteras för att påverka hur det resulterande dokumentet visas i den visuella agenten (t.ex. en webbläsare eller visare).

Använd den här egenskapen som ett filter för att ange vilka tabellbredder som exporteras till destinationsdokumentet. Till exempel, om du konverterar ett dokument till EPUB och avser att visa dokumentet på en mobil läsenhet, vill du sannolikt undvika att exportera absoluta breddvärden. För att göra detta måste du ange utskriftsläget [RelativeOnly](../../htmlelementsizeoutputmode/) eller [None](../../htmlelementsizeoutputmode/) så att visaren på den mobila enheten kan layouta tabellen så att den passar skärmens bredd så bra som möjligt.

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

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

---
title: HtmlSaveOptions.AllowNegativeIndent
linktitle: AllowNegativeIndent
articleTitle: AllowNegativeIndent
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions AllowNegativeIndent för att styra styckeindrag när du sparar till HTML, MHTML eller EPUB. Optimera din dokumentformatering idag!
type: docs
weight: 20
url: /sv/net/aspose.words.saving/htmlsaveoptions/allownegativeindent/
---
## HtmlSaveOptions.AllowNegativeIndent property

Anger om negativa vänster- och högerindrag i stycken normaliseras när de sparas i HTML, MHTML eller EPUB. Standardvärdet är`falsk` .

```csharp
public bool AllowNegativeIndent { get; set; }
```

## Anmärkningar

När negativt indrag inte är tillåtet exporteras det som nollmarginal till HTML. När negativt indrag är tillåtet kan ett stycke delvis visas utanför webbläsarfönstret .

## Exempel

Visar hur man bevarar negativa indent i utdata-.html-filen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en tabell med ett negativt indrag, vilket flyttar den åt vänster förbi den vänstra sidgränsen.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Infoga en tabell med ett positivt indrag, vilket flyttar tabellen åt höger.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// När vi sparar ett dokument till HTML, kommer Aspose.Words bara att bevara negativa indrag
// som den vi har tillämpat på den första tabellen om vi sätter flaggan "AllowNegativeIndent"
// i ett SaveOptions-objekt som vi skickar till "true".
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    AllowNegativeIndent = allowNegativeIndent,
    TableWidthOutputMode = HtmlElementSizeOutputMode.RelativeOnly
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

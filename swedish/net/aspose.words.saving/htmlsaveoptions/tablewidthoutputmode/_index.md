---
title: HtmlSaveOptions.TableWidthOutputMode
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Styr hur tabell rad och cellbredder exporteras till HTML MHTML eller EPUB. Standardvärdet ärAll .
type: docs
weight: 460
url: /sv/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Styr hur tabell-, rad- och cellbredder exporteras till HTML, MHTML eller EPUB. Standardvärdet ärAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

### Anmärkningar

HTML-formatet, tabell-, rad- och cellelement ( **&lt;tabell&gt;** , **&lt;tr&gt;** , **&lt;th&gt;** , **&lt;td&gt;**) kan ha sina bredder specificerade antingen i relativ (procent) eller i absoluta enheter. I ett dokument i Aspose. Words, tabeller, rader och celler kan ha sina bredder specificerade med antingen relativa eller absoluta enheter.

När du konverterar ett dokument till HTML med Aspose.Words kanske du vill kontrollera hur tabell-, rad- och cellbredder exporteras för att påverka hur det resulterande dokumentet visas i den visuella agenten (t.ex. en webbläsare eller visningsprogram).

Använd den här egenskapen som ett filter för att ange vilka tabellbreddsvärden som ska exporteras till måldokumentet. Om du till exempel konverterar ett dokument till EPUB och tänker visa dokumentet på en mobil läsenhet, vill du förmodligen undvika exporterar absoluta breddvärden. För att göra detta måste du ange utgångslägetRelativeOnly ellerNone så att tittaren på den mobila enheten kan layouta tabellen så att den passar skärmens bredd så bra som den kan.

### Exempel

Visar hur man bevarar negativa indrag i utdata .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en tabell med ett negativt indrag, vilket kommer att skjuta den till vänster förbi den vänstra sidgränsen.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Infoga en tabell med ett positivt indrag, vilket kommer att skjuta tabellen åt höger.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// När vi sparar ett dokument till HTML kommer Aspose.Words endast att bevara negativa indrag
// som den vi har tillämpat på den första tabellen om vi ställer in flaggan "AllowNegativeIndent"
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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)



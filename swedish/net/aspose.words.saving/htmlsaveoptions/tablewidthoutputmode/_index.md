---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: Aspose.Words för .NET
description: Optimera dina HTML-exporter med HtmlSaveOptions TableWidthOutputMode. Kontrollera rad- och cellbredder i tabeller för sömlös MHTML- och EPUB-formatering.
type: docs
weight: 480
url: /sv/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Styr hur tabell-, rad- och cellbredder exporteras till HTML, MHTML eller EPUB. Standardvärdet ärAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## Anmärkningar

HTML-formatet, tabell-, rad- och cellelement (**&lt;tabell&gt;** ,**&lt;tr&gt;** ,**&lt;e&gt;** ,**&lt;td&gt;**) kan få sina bredder angivna antingen i relativa (procent) eller i absoluta enheter. I ett dokument i Aspose. Ord, tabeller, rader och celler kan också få sina bredder angivna med antingen relativa eller absoluta enheter.

När du konverterar ett dokument till HTML med Aspose.Words kanske du vill kontrollera hur tabell-, rad- och cellbredder exporteras för att påverka hur det resulterande dokumentet visas i den visuella agenten (t.ex. en webbläsare eller ett visningsprogram).

Använd den här egenskapen som ett filter för att ange vilka tabellbredder som exporteras till destinationsdokumentet. Om du till exempel konverterar ett dokument till EPUB och avser att visa dokumentet på en mobil läsenhet, vill du förmodligen undvika att exportera absoluta breddvärden. För att göra detta måste du ange utdataläget.RelativeOnly ellerNone så att tittaren på den mobila enheten kan utforma tabellen så att den passar skärmens bredd så bra som möjligt.

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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

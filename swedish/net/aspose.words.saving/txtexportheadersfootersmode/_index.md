---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words TxtExportHeadersFootersMode-enum förbättrar export av vanlig text genom att anpassa hanteringen av sidhuvud och sidfot för optimala resultat.
type: docs
weight: 6440
url: /sv/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

Anger hur sidhuvuden och sidfot exporteras till vanligt textformat.

```csharp
public enum TxtExportHeadersFootersMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Inga sidhuvuden och sidfot exporteras. |
| PrimaryOnly | `1` | Endast primära sidhuvuden och sidfot exporteras i början och slutet av varje avsnitt. |
| AllAtEnd | `2` | Alla sidhuvuden och sidfot placeras efter alla avsnittstexter i slutet av ett dokument. |

## Exempel

Visar hur man anger hur man exporterar sidhuvuden och sidfot till vanligt textformat.

```csharp
Document doc = new Document();

// Infoga jämna och primära sidhuvuden/sidfot i dokumentet.
// Primära sidhuvuden/sidfötter kommer att åsidosätta de jämna sidhuvudena/sidfötterna.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Infoga sidor för att visa dessa sidhuvuden och sidfot.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Ställ in egenskapen "ExportHeadersFootersMode" till "TxtExportHeadersFootersMode.None"
// för att inte exportera några sidhuvuden/sidfot.
// Ställ in egenskapen "ExportHeadersFootersMode" till "TxtExportHeadersFootersMode.PrimaryOnly"
// för att endast exportera primära sidhuvuden/sidfot.
// Ställ in egenskapen "ExportHeadersFootersMode" till "TxtExportHeadersFootersMode.AllAtEnd"
// för att placera alla sidhuvuden och sidfot för alla avsnittstexter i slutet av dokumentet.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

string newLine = Environment.NewLine;
switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Even header{newLine}{newLine}" +
                        $"Primary header{newLine}{newLine}" +
                        $"Even footer{newLine}{newLine}" +
                        $"Primary footer{newLine}{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual($"Primary header{newLine}" +
                        $"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Primary footer{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}", docText);
        break;
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)

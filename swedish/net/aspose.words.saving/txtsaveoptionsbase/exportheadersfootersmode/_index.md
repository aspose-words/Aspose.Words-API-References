---
title: TxtSaveOptionsBase.ExportHeadersFootersMode
second_title: Aspose.Words för .NET API Referens
description: TxtSaveOptionsBase fast egendom. Anger hur sidhuvuden och sidfötter exporteras till textformaten. Standardvärdet ärPrimaryOnly .
type: docs
weight: 20
url: /sv/net/aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/
---
## TxtSaveOptionsBase.ExportHeadersFootersMode property

Anger hur sidhuvuden och sidfötter exporteras till textformaten. Standardvärdet ärPrimaryOnly .

```csharp
public TxtExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

### Exempel

Visar hur man anger hur man exporterar sidhuvuden och sidfötter till vanligt textformat.

```csharp
Document doc = new Document();

// Infoga jämna och primära sidhuvuden/sidfötter i dokumentet.
// De primära sidhuvuden/sidfötterna kommer att åsidosätta de jämna sidhuvuden/sidfötterna.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Infoga sidor för att visa dessa sidhuvuden och sidfötter.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Ställ in egenskapen "ExportHeadersFootersMode" till "TxtExportHeadersFootersMode.None"
// för att inte exportera några sidhuvuden/sidfötter.
// Ställ in egenskapen "ExportHeadersFootersMode" till "TxtExportHeadersFootersMode.PrimaryOnly"
// för att endast exportera primära sidhuvuden/sidfötter.
// Ställ in egenskapen "ExportHeadersFootersMode" till "TxtExportHeadersFootersMode.AllAtEnd"
// för att placera alla sidhuvuden och sidfötter för alla avsnittskroppar i slutet av dokumentet.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Even header\r\n\r\n" +
                        "Primary header\r\n\r\n" +
                        "Even footer\r\n\r\n" +
                        "Primary footer\r\n\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual("Primary header\r\n" +
                        "Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Primary footer\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n", docText);
        break;
}
```

### Se även

* enum [TxtExportHeadersFootersMode](../../txtexportheadersfootersmode/)
* class [TxtSaveOptionsBase](../)
* namnutrymme [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* hopsättning [Aspose.Words](../../../)



---
title: ExportRoundtripInformation
second_title: Aspose.Words för .NET API Referens
description: Anger om informationen tur och retur ska skrivas när du sparar till HTML MHTML eller EPUB. Standardvärdet ärSann för HTML ochfalsk för MHTML och EPUB.
type: docs
weight: 250
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Anger om informationen tur och retur ska skrivas när du sparar till HTML, MHTML eller EPUB. Standardvärdet är`Sann` för HTML och`falsk` för MHTML och EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

### Anmärkningar

Genom att spara informationen tur och retur kan du återställa dokumentegenskaper som tabbstopp, kommentarer, sidhuvuden och sidfötter när HTML-dokumenten laddas tillbaka till en[`Document`](../../../aspose.words/document/) objekt.

När`Sann`, exporteras informationen tur och retur som -aw-* CSS properties för motsvarande HTML-element.

När`falsk`, gör att ingen information tur och retur matas ut till producerade filer.

### Exempel

Visar hur man bevarar dolda element vid konvertering till .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// När du konverterar ett dokument till .html, vissa element som dolda bokmärken, ursprungliga formpositioner,
// eller fotnoter kommer antingen att tas bort eller konverteras till vanlig text och försvinner i praktiken.
// Att spara med ett HtmlSaveOptions-objekt med ExportRoundtripInformation satt till true kommer att bevara dessa element.

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt för att fastställa
// hur sparoperationen kommer att exportera dokumentelement som HTML inte stöder eller använder,
// som dolda bokmärken och ursprungliga formpositioner.
// Om vi ställer in "ExportRoundtripInformation"-flaggan till "true", kommer spara-operationen att bevara dessa element.
// Om vi ställer in "ExportRoundTripInformation"-flaggan till "false", kommer spara-operationen att förkasta dessa element.
// Vi kommer att vilja bevara sådana element om vi tänker ladda den sparade HTML-koden med Aspose.Words,
// eftersom de skulle kunna vara till nytta igen.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.True(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    Assert.True(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"));

    Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
else
{
    Assert.True(outDocContents.Contains("<div style=\"clear:both\">"));
    Assert.True(outDocContents.Contains("<span>&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number 1</span>"));

    Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

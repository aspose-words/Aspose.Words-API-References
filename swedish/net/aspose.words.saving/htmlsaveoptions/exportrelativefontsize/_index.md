---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions ExportRelativeFontSize för att anpassa teckenstorlekar i HTML-, MHTML- eller EPUB-format. Förbättra läsbarheten med lätthet!
type: docs
weight: 230
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

Anger om teckenstorlekar ska matas ut i relativa enheter när man sparar till HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## Anmärkningar

många befintliga dokument (HTML, IDPF EPUB) anges teckenstorlekar i relativa enheter. Detta gör det möjligt för -applikationer att justera textstorleken när de visar/bearbetar dokument. Till exempel har Microsoft Internet Explorer en undermeny "Visa-&gt;Textstorlek", medan Adobe Digital Editions har två knappar: Öka/Minska textstorlek. Om du förväntar dig att den här funktionen ska fungera, ställ in`ExportRelativeFontSize` egendom till`sann` .

Aspose Words-dokumentmodellen innehåller och fungerar endast med absoluta teckenstorleksenheter. Relativa enheter behöver ytterligare logik för att beräknas om från en initial (standard) storlek. Teckenstorlek för**Normal** dokumentstil används som standard. Till exempel, om**Normal** har 12pt-teckensnitt och en del text är 18pt så kommer det att visas som **1,5 em.** till HTML-koden.

När det här alternativet är aktiverat kommer andra dokumentelement än text fortfarande att ha absoluta storlekar. Även vissa textrelaterade attribut kan uttryckas absolut. I synnerhet kan radavstånd som anges med rule "exakt" ge oönskade resultat vid skalning av text. Så källdokumenten bör vara korrekt utformade och testade vid export med`ExportRelativeFontSize` inställd på`sann`.

## Exempel

Visar hur man använder relativa teckenstorlekar när man sparar till .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att avgöra om relativa eller absoluta teckenstorlekar ska användas.
// Sätt flaggan "ExportRelativeFontSize" till "true" för att deklarera teckenstorlekar
 // med hjälp av måttenheten "em", vilket är en faktor som multiplicerar den aktuella teckenstorleken.
// Sätt flaggan "ExportRelativeFontSize" till "false" för att deklarera teckenstorlekar
// använder måttenheten "pt", vilket är teckensnittets absoluta storlek i punkter.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRelativeFontSize = exportRelativeFontSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

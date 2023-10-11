---
title: HtmlSaveOptions.ExportRelativeFontSize
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger om teckenstorlekar ska matas ut i relativa enheter när du sparar till HTML MHTML eller EPUB. Standard ärfalsk .
type: docs
weight: 230
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

Anger om teckenstorlekar ska matas ut i relativa enheter när du sparar till HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

### Anmärkningar

många befintliga dokument (HTML, IDPF EPUB) anges teckenstorlekar i relativa enheter. Detta gör det möjligt för -applikationer att justera textstorleken vid visning/bearbetning av dokument. Till exempel har Microsoft Internet Explorer undermenyn "Visa-&gt;Textstorlek", Adobe Digital Editions har två knappar: Öka/minska textstorlek. Om du förväntar dig att den här funktionen ska fungera, ställ in`ExportRelativeFontSize` egendom till`Sann` .

Aspose Words dokumentmodell innehåller och fungerar endast med absoluta teckenstorleksenheter. Relativa enheter behöver ytterligare logik för att beräknas om från någon initial (standard) storlek. Teckenstorlek på **Vanligt** dokumentstil tas som standard. Till exempel om **Vanligt** har 12 pkt teckensnitt och viss text är 18 pkt så kommer den att matas ut som **1,5 em.** till HTML.

När det här alternativet är aktiverat kommer andra dokumentelement än text fortfarande att ha absoluta storlekar. Vissa textrelaterade attribut kan också uttryckas absolut. I synnerhet radavstånd som anges med "exakt" regeln kan ge oönskade resultat vid skalning av text. Så källdokumenten bör vara korrekt designade och testade vid export med`ExportRelativeFontSize` satt till`Sann`.

### Exempel

Visar hur du använder relativa teckenstorlekar när du sparar till .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att avgöra om du ska använda relativa eller absoluta teckenstorlekar.
// Ställ in "ExportRelativeFontSize"-flaggan till "true" för att deklarera teckenstorlekar
 // med hjälp av måtten "em", vilket är en faktor som multiplicerar den aktuella teckenstorleken.
// Ställ in "ExportRelativeFontSize"-flaggan till "false" för att deklarera teckenstorlekar
// med hjälp av måttenheten "pt", som är teckensnittets absoluta storlek i poäng.
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
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)



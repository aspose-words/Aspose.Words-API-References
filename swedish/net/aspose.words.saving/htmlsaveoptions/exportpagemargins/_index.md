---
title: HtmlSaveOptions.ExportPageMargins
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger om sidmarginaler exporteras till HTML MHTML eller EPUB. Standard ärfalsk .
type: docs
weight: 210
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Anger om sidmarginaler exporteras till HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportPageMargins { get; set; }
```

### Anmärkningar

Aspose.Words visar inte område med sidmarginaler som standard. Om några element är helt eller delvis klippta av dokumentkanten kan det visade området utökas med detta alternativ.

### Exempel

Visar hur man visar out-of-bounds-objekt i utgående HTML-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en builder för att infoga en form utan omslag.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Negativa formpositionsvärden kan placera formen utanför sidgränserna.
// Om vi exporterar detta till HTML kommer formen att se trunkerad ut.
shape.Left = -150;

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma om sidan ska justeras för att visa out-of-bound-objekt helt.
// Om vi ställer in "ExportPageMargins"-flaggan till "true", kommer formen att vara helt synlig i utdata-HTML.
// Om vi ställer in flaggan "ExportPageMargins" till "false",
// vårt dokument kommer att visa formen trunkerad som vi skulle se den i Microsoft Word.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)



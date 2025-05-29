---
title: HtmlSaveOptions.ExportPageMargins
linktitle: ExportPageMargins
articleTitle: ExportPageMargins
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlSaveOptions ExportPageMargins förbättrar dina HTML-, MHTML- och EPUB-exporter genom att styra sidmarginalerna för en elegant presentation.
type: docs
weight: 210
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Anger om sidmarginaler exporteras till HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportPageMargins { get; set; }
```

## Anmärkningar

Aspose.Words visar inte sidmarginalerna som standard. Om några element är helt eller delvis klippta av dokumentkanten kan det visade området utökas med det här alternativet.

## Exempel

Visar hur man visar objekt utanför gränserna i HTML-utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en verktygsbyggare för att infoga en form utan radbrytning.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Negativa värden för formpositionering kan placera formen utanför sidans gränser.
// Om vi exporterar detta till HTML kommer formen att se avkortad ut.
shape.Left = -150;

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma om sidan ska justeras för att visa objekt utanför gränserna helt.
// Om vi ställer in flaggan "ExportPageMargins" till "true" kommer formen att synas helt i HTML-utdata.
// Om vi ställer in flaggan "ExportPageMargins" till "false",
// vårt dokument kommer att visa formen avkortad som vi skulle se den i Microsoft Word.
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
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

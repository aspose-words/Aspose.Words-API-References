---
title: PageSetup.BorderSurroundsFooter
linktitle: BorderSurroundsFooter
articleTitle: BorderSurroundsFooter
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen PageSetup BorderSurroundsFooter kan förbättra din dokumentlayout genom att styra inkludering av sidfot i sidkanter.
type: docs
weight: 60
url: /sv/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

Anger om sidkanten inkluderar eller exkluderar sidfoten.

```csharp
public bool BorderSurroundsFooter { get; set; }
```

## Anmärkningar

Observera att ändring av den här egenskapen påverkar alla avsnitt i dokumentet.

## Exempel

Visar hur man applicerar en kantlinje på sidan och sidhuvudet/sidfoten.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Infoga en blå dubbellinjeram.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// En sektions PageSetup-objekt har flaggorna "BorderSurroundsHeader" och "BorderSurroundsFooter" som avgör
// om en sidkantlinje omger huvudtexten, även inkluderar sidhuvudet respektive sidfoten.
// Sätt flaggan "BorderSurroundsHeader" till "true" för att omge sidhuvudet med vår kantlinje,
// och sätt sedan flaggan "BorderSurroundsFooter" för att lämna sidfoten utanför ramen.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

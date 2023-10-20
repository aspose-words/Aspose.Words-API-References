---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: Aspose.Words för .NET
description: PageSetup BorderSurroundsHeader fast egendom. Anger om sidkanten inkluderar eller exkluderar rubriken i C#.
type: docs
weight: 70
url: /sv/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

Anger om sidkanten inkluderar eller exkluderar rubriken.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## Anmärkningar

Obs, att ändra den här egenskapen påverkar alla avsnitt i dokumentet.

## Exempel

Visar hur man använder en ram på sidan och sidhuvud/sidfot.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Infoga en blå dubbellinjekant.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// En sektions PageSetup-objekt har flaggorna "BorderSurroundsHeader" och "BorderSurroundsFooter" som bestämmer
// om en sidkant omger huvudtexten, inkluderar även sidhuvudet respektive sidfoten.
// Ställ in "BorderSurroundsHeader"-flaggan till "true" för att omge rubriken med vår kant,
// och ställ sedan in "BorderSurroundsFooter"-flaggan för att lämna sidfoten utanför gränsen.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

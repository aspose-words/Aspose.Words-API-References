---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen CreateOutlinesForHeadingsInTables förbättrar tabellorganisationen genom att aktivera konturer för rubrikformat, vilket förbättrar dokumentets tydlighet.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Anger om dispositioner ska skapas för rubriker (stycken formaterade med rubrikformat) inuti tabeller.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`.

## Exempel

Visar hur man skapar dispositionsposter i PDF-dokument för rubriker inuti tabeller.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en tabell med tre rader. Den första raden,
// vars text vi formaterar i rubrikformat, kommer att fungera som kolumnrubrik.
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Det utgående PDF-dokumentet kommer att innehålla en disposition, vilket är en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Om du klickar på en post i den här dispositionen kommer vi till platsen för respektive rubrik.
// Sätt egenskapen "HeadingsOutlineLevels" till "1" för att hämta dispositionen
// för att endast registrera rubriker med rubriknivåer som inte är större än 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Sätt egenskapen "CreateOutlinesForHeadingsInTables" till "false" för att exkludera alla rubriker i tabeller,
// som den vi har skapat ovan från dispositionen.
// Sätt egenskapen "CreateOutlinesForHeadingsInTables" till "true" för att inkludera alla rubriker i tabeller
// i dispositionen, förutsatt att de har en rubriknivå som inte är större än värdet för egenskapen "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Se även

* class [OutlineOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

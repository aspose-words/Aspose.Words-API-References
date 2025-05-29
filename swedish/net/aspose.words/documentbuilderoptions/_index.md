---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.DocumentBuilderOptions för att förbättra ditt dokumentskapande med anpassningsbara funktioner för en sömlös byggupplevelse.
type: docs
weight: 670
url: /sv/net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

Gör det möjligt att ange ytterligare alternativ för dokumentbyggprocessen.

```csharp
public class DocumentBuilderOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | Sant om formateringen som tillämpas på tabellinnehållet inte påverkar formateringen av innehållet som följer. Standardvärdet är`sann` . |
| [DesignMode](../../aspose.words/documentbuilderoptions/designmode/) { get; set; } | Motsvarar designläget i Microsoft Word. |

## Exempel

Visar hur man ignorerar tabellformatering för innehåll efteråt.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Lägger till innehåll före tabellen.
// Standardteckenstorleken är 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Ändrar teckenstorleken inuti tabellen.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Om ContextTableFormatting är sant, tillämpas inte tabellformatering på innehållet efteråt.
// Om ContextTableFormatting är falskt, tillämpas tabellformatering på innehållet efteråt.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)

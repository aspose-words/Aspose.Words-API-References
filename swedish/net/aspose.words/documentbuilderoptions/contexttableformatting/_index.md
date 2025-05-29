---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ContextTableFormatting i DocumentBuilderOptions. Se till att tabellformateringen förblir oberoende, vilket förbättrar dokumentets tydlighet och stil.
type: docs
weight: 20
url: /sv/net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

Sant om formateringen som tillämpas på tabellinnehållet inte påverkar formateringen av innehållet som följer. Standardvärdet är`sann` .

```csharp
public bool ContextTableFormatting { get; set; }
```

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

* class [DocumentBuilderOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

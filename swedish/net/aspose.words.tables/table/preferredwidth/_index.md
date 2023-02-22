---
title: Table.PreferredWidth
second_title: Aspose.Words för .NET API Referens
description: Table fast egendom. Hämtar eller ställer in tabellens föredragna bredd.
type: docs
weight: 220
url: /sv/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

Hämtar eller ställer in tabellens föredragna bredd.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

### Anmärkningar

Standardvärdet är[`Auto`](../../preferredwidth/auto/).

### Exempel

Visar hur du ställer in en tabell för att automatiskt anpassa till 50 % av sidans bredd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

### Se även

* class [PreferredWidth](../../preferredwidth/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../table/)
* hopsättning [Aspose.Words](../../../)



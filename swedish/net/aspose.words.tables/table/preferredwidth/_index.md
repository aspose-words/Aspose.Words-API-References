---
title: Table.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen Table PreferredWidth för att enkelt ställa in och optimera tabellens layout för förbättrad design och användarupplevelse.
type: docs
weight: 220
url: /sv/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

Hämtar eller ställer in tabellens önskade bredd.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Anmärkningar

Standardvärdet är[`Auto`](../../preferredwidth/auto/).

## Exempel

Visar hur man ställer in en tabell så att den automatiskt anpassas till 50 % av sidans bredd.

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
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)

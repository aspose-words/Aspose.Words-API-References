---
title: Table.PreferredWidth
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Ottiene o imposta la larghezza preferita della tabella.
type: docs
weight: 220
url: /it/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

Ottiene o imposta la larghezza preferita della tabella.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

### Osservazioni

Il valore predefinito è[`Auto`](../../preferredwidth/auto/).

### Esempi

Mostra come impostare una tabella in modo che si adatti automaticamente al 50% della larghezza della pagina.

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

### Guarda anche

* class [PreferredWidth](../../preferredwidth/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)



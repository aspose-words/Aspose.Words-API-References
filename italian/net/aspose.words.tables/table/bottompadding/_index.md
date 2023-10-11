---
title: Table.BottomPadding
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Ottiene o imposta la quantità di spazio in punti da aggiungere sotto il contenuto delle celle.
type: docs
weight: 90
url: /it/net/aspose.words.tables/table/bottompadding/
---
## Table.BottomPadding property

Ottiene o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto delle celle.

```csharp
public double BottomPadding { get; set; }
```

### Esempi

Mostra come configurare il riempimento del contenuto in una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // Per ogni cella della tabella, imposta la distanza tra il suo contenuto e ciascuno dei suoi bordi.
// Questa tabella manterrà la distanza minima di riempimento mandando a capo il testo.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)



---
title: Table.RelativeVerticalAlignment
linktitle: RelativeVerticalAlignment
articleTitle: RelativeVerticalAlignment
second_title: Aspose.Words per .NET
description: Table RelativeVerticalAlignment proprietà. Ottiene o imposta lallineamento verticale relativo della tabella mobile in C#.
type: docs
weight: 240
url: /it/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

Ottiene o imposta l'allineamento verticale relativo della tabella mobile.

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
```

## Esempi

Mostra come impostare la posizione delle tabelle mobili.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Imposta la posizione della tabella su un punto della pagina, come, in questo caso, l'angolo in basso a destra.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Possiamo anche impostare uno spostamento orizzontale e verticale in punti dalla posizione del paragrafo in cui abbiamo inserito la tabella.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Guarda anche

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)

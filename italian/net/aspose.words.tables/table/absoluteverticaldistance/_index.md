---
title: Table.AbsoluteVerticalDistance
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Ottiene o imposta la posizione assoluta della tabella mobile verticale specificata dalle proprietà della tabella in punti. Il valore predefinito è 0.
type: docs
weight: 30
url: /it/net/aspose.words.tables/table/absoluteverticaldistance/
---
## Table.AbsoluteVerticalDistance property

Ottiene o imposta la posizione assoluta della tabella mobile verticale specificata dalle proprietà della tabella, in punti. Il valore predefinito è 0.

```csharp
public double AbsoluteVerticalDistance { get; set; }
```

### Esempi

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

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)



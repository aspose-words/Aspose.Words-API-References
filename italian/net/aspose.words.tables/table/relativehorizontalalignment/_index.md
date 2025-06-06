---
title: Table.RelativeHorizontalAlignment
linktitle: RelativeHorizontalAlignment
articleTitle: RelativeHorizontalAlignment
second_title: Aspose.Words per .NET
description: Scopri la proprietà Table RelativeHorizontalAlignment per regolare facilmente l'allineamento orizzontale della tabella, per un controllo migliore del layout e un impatto visivo migliore.
type: docs
weight: 230
url: /it/net/aspose.words.tables/table/relativehorizontalalignment/
---
## Table.RelativeHorizontalAlignment property

Ottiene o imposta l'allineamento orizzontale relativo della tabella mobile.

```csharp
public HorizontalAlignment RelativeHorizontalAlignment { get; set; }
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

// Imposta la posizione della tabella in un punto della pagina, ad esempio, in questo caso, l'angolo in basso a destra.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Possiamo anche impostare uno scostamento orizzontale e verticale in punti dalla posizione del paragrafo in cui abbiamo inserito la tabella.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Guarda anche

* enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)

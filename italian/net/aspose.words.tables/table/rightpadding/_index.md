---
title: Table.RightPadding
linktitle: RightPadding
articleTitle: RightPadding
second_title: Aspose.Words per .NET
description: Scopri la proprietà "Tabella RightPadding" per personalizzare la spaziatura delle celle. Regola facilmente il margine destro per migliorare il layout e la leggibilità dei tuoi progetti.
type: docs
weight: 250
url: /it/net/aspose.words.tables/table/rightpadding/
---
## Table.RightPadding property

Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle.

```csharp
public double RightPadding { get; set; }
```

## Esempi

Mostra come configurare la spaziatura del contenuto in una tabella.

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
// Questa tabella manterrà la distanza minima di padding mediante l'inserimento del testo.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)

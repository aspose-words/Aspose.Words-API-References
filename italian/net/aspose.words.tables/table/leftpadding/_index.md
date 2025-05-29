---
title: Table.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words per .NET
description: Scopri la proprietà Table LeftPadding, regola facilmente la spaziatura del contenuto delle celle in punti per un controllo migliorato del layout e una maggiore flessibilità di progettazione.
type: docs
weight: 200
url: /it/net/aspose.words.tables/table/leftpadding/
---
## Table.LeftPadding property

Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle.

```csharp
public double LeftPadding { get; set; }
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

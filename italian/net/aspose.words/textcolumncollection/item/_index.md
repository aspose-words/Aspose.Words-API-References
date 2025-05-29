---
title: TextColumnCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi a una colonna di testo specifica tramite indice con la proprietà TextColumnCollection Item. Semplifica la gestione dei dati e migliora l'efficienza della tua programmazione.
type: docs
weight: 30
url: /it/net/aspose.words/textcolumncollection/item/
---
## TextColumnCollection indexer

Restituisce una colonna di testo all'indice specificato.

```csharp
public TextColumn this[int index] { get; }
```

## Esempi

Mostra come creare colonne con spaziature non uniformi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Determinare la quantità di spazio disponibile per disporre le colonne.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Imposta la prima colonna in modo che sia stretta.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Imposta la seconda colonna in modo che occupi il resto dello spazio disponibile entro i margini della pagina.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Guarda anche

* class [TextColumn](../../textcolumn/)
* class [TextColumnCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

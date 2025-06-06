---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextColumn SpaceAfter per regolare facilmente la spaziatura tra le colonne del tuo layout. Migliora la leggibilità e il design con precisione!
type: docs
weight: 10
url: /it/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Ottiene o imposta lo spazio tra questa colonna e la colonna successiva in punti. Non richiesto per l'ultima colonna.

```csharp
public double SpaceAfter { get; set; }
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

* class [TextColumn](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

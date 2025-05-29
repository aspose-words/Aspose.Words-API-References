---
title: TextColumnCollection.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextColumnCollection Spacing e gestisci facilmente la spaziatura delle colonne in punti per un layout curato e professionale. Migliora il tuo design oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

Quando le colonne sono distanziate uniformemente, ottiene o imposta la quantità di spazio tra ciascuna colonna in punti.

```csharp
public double Spacing { get; set; }
```

## Osservazioni

Ha effetto solo quando[`EvenlySpaced`](../evenlyspaced/) è impostato su`VERO` .

## Esempi

Mostra come creare più colonne equidistanti in una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Guarda anche

* class [TextColumnCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

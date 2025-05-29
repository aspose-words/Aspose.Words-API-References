---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words per .NET
description: Scopri la proprietà Larghezza di TextColumnCollection. Gestisci facilmente colonne con spaziatura uniforme per un layout e un design ottimali nei tuoi progetti.
type: docs
weight: 60
url: /it/net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

Quando le colonne sono distanziate uniformemente, ottiene la larghezza delle colonne.

```csharp
public double Width { get; }
```

## Osservazioni

Ha effetto solo quando[`EvenlySpaced`](../evenlyspaced/) è impostato su`VERO`.

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

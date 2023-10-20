---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: Aspose.Words per .NET
description: PageSetup TextColumns proprietà. Restituisce una raccolta che rappresenta linsieme di colonne di testo in C#.
type: docs
weight: 420
url: /it/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Restituisce una raccolta che rappresenta l'insieme di colonne di testo.

```csharp
public TextColumnCollection TextColumns { get; }
```

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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

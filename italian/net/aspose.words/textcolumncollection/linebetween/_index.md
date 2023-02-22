---
title: TextColumnCollection.LineBetween
second_title: Aspose.Words per .NET API Reference
description: TextColumnCollection proprietà. Quando VERO  aggiunge una linea verticale tra le colonne.
type: docs
weight: 40
url: /it/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

Quando **VERO** , aggiunge una linea verticale tra le colonne.

```csharp
public bool LineBetween { get; set; }
```

### Esempi

Mostra come separare le colonne con una linea verticale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configura l'oggetto PageSetup della sezione corrente per dividere il testo in più colonne.
// Imposta la proprietà "LineBetween" su "true" per inserire una linea di demarcazione tra le colonne.
// Imposta la proprietà "LineBetween" su "false" per lasciare vuoto lo spazio tra le colonne.
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.LineBetween = lineBetween;
columns.SetCount(3);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 3.");

doc.Save(ArtifactsDir + "PageSetup.VerticalLineBetweenColumns.docx");
```

### Guarda anche

* class [TextColumnCollection](../)
* spazio dei nomi [Aspose.Words](../../textcolumncollection/)
* assemblea [Aspose.Words](../../../)



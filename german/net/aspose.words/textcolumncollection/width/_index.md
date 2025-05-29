---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „TextColumnCollection Width“. Verwalten Sie mühelos gleichmäßig verteilte Spalten für optimales Layout und Design in Ihren Projekten.
type: docs
weight: 60
url: /de/net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

Wenn die Spalten gleichmäßig verteilt sind, wird die Breite der Spalten abgerufen.

```csharp
public double Width { get; }
```

## Bemerkungen

Wirkt nur, wenn[`EvenlySpaced`](../evenlyspaced/) ist eingestellt auf`WAHR`.

## Beispiele

Zeigt, wie mehrere gleichmäßig verteilte Spalten in einem Abschnitt erstellt werden.

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

### Siehe auch

* class [TextColumnCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

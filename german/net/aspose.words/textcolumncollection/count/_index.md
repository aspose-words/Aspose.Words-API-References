---
title: TextColumnCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „TextColumnCollection Count“, um einfach auf die Anzahl der Spalten im Abschnitt Ihres Dokuments zuzugreifen und so die Layoutsteuerung zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words/textcolumncollection/count/
---
## TextColumnCollection.Count property

Ruft die Anzahl der Spalten im Abschnitt eines Dokuments ab.

```csharp
public int Count { get; }
```

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

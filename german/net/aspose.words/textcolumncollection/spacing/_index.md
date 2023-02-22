---
title: TextColumnCollection.Spacing
second_title: Aspose.Words für .NET-API-Referenz
description: TextColumnCollection eigendom. Ruft bei gleichmäßigen Spaltenabständen den Abstand zwischen den einzelnen Spalten in Punkten ab oder legt ihn fest.
type: docs
weight: 50
url: /de/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

Ruft bei gleichmäßigen Spaltenabständen den Abstand zwischen den einzelnen Spalten in Punkten ab oder legt ihn fest.

```csharp
public double Spacing { get; set; }
```

### Bemerkungen

Hat nur Wirkung, wenn[`EvenlySpaced`](../evenlyspaced/) ist eingestellt auf **Stimmt** .

### Beispiele

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
* namensraum [Aspose.Words](../../textcolumncollection/)
* Montage [Aspose.Words](../../../)



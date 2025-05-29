---
title: TextColumnCollection.LineBetween
linktitle: LineBetween
articleTitle: LineBetween
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihr Layout mit der Eigenschaft „LineBetween“ der TextColumnCollection. Aktivieren Sie vertikale Linien zwischen Spalten für ein elegantes, übersichtliches Erscheinungsbild.
type: docs
weight: 40
url: /de/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

Wann`WAHR` , fügt eine vertikale Linie zwischen den Spalten hinzu.

```csharp
public bool LineBetween { get; set; }
```

## Beispiele

Zeigt, wie Spalten mit einer vertikalen Linie getrennt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Konfigurieren Sie das PageSetup-Objekt des aktuellen Abschnitts, um den Text in mehrere Spalten aufzuteilen.
// Setzen Sie die Eigenschaft „LineBetween“ auf „true“, um eine Trennlinie zwischen den Spalten einzufügen.
// Setzen Sie die Eigenschaft „LineBetween“ auf „false“, um den Abstand zwischen den Spalten leer zu lassen.
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

### Siehe auch

* class [TextColumnCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

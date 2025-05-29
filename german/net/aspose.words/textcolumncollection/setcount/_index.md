---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr Layout mit der SetCount-Methode von TextColumnCollection und ordnen Sie Text mühelos in der gewünschten Anzahl von Spalten an, um die Lesbarkeit zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Ordnet Text in die angegebene Anzahl von Textspalten an.

```csharp
public void SetCount(int newCount)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newCount | Int32 | Die Anzahl der Spalten, in denen der Text angeordnet werden soll. |

## Bemerkungen

Wann[`EvenlySpaced`](../evenlyspaced/) Ist`FALSCH` und Sie erhöhen die Anzahl der Spalten, neue[`TextColumn`](../../textcolumn/) Objekte werden mit einer Breite und einem Abstand von Null erstellt. Sie müssen die Breite und den Abstand für die neuen Spalten festlegen.

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

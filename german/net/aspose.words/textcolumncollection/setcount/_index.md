---
title: TextColumnCollection.SetCount
second_title: Aspose.Words für .NET-API-Referenz
description: TextColumnCollection methode. Ordnet Text in der angegebenen Anzahl von Textspalten an.
type: docs
weight: 70
url: /de/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Ordnet Text in der angegebenen Anzahl von Textspalten an.

```csharp
public void SetCount(int newCount)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newCount | Int32 | Die Anzahl der Spalten, in die der Text angeordnet werden soll. |

### Bemerkungen

Wann[`EvenlySpaced`](../evenlyspaced/) Ist`FALSCH` und Sie erhöhen die Anzahl der Spalten, neu[`TextColumn`](../../textcolumn/) Objekte werden mit einer Breite und einem Abstand von Null erstellt. Sie müssen Breite und Abstand für die neuen Spalten festlegen.

### Beispiele

Zeigt, wie Sie mehrere gleichmäßig verteilte Spalten in einem Abschnitt erstellen.

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



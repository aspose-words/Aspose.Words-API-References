---
title: DocumentBuilder.DeleteRow
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Löscht eine Zeile aus einer Tabelle.
type: docs
weight: 180
url: /de/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Löscht eine Zeile aus einer Tabelle.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableIndex | Int32 | Der Index der Tabelle. |
| rowIndex | Int32 | Der Index der Zeile in der Tabelle. |

### Rückgabewert

Der Zeilenknoten, der gerade entfernt wurde.

### Bemerkungen

Wenn sich der Cursor in der zu löschenden Zeile befindet, wird der Cursor in die nächste Zeile oder in den nächsten Absatz nach der Tabelle verschoben .

Wenn Sie eine Zeile aus einer Tabelle löschen, die nur eine Zeile enthält, wird die Tabelle whole gelöscht.

Wenn Index größer oder gleich 0 ist, wird für die Indexparameter ein Index von am Anfang angegeben, wobei 0 das erste Element ist. Wenn der Index kleiner als 0 ist, wurde ein Index from the end angegeben, wobei -1 das letzte Element ist.

### Beispiele

Zeigt, wie eine Zeile aus einer Tabelle gelöscht wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.AreEqual(2, table.Rows.Count);

// Löschen Sie die erste Zeile der ersten Tabelle im Dokument.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### Siehe auch

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)



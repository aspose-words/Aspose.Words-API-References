---
title: DocumentBuilder.MoveToCell
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Bewegt den Cursor zu einer Tabellenzelle im aktuellen Abschnitt.
type: docs
weight: 480
url: /de/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

Bewegt den Cursor zu einer Tabellenzelle im aktuellen Abschnitt.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableIndex | Int32 | Der Index der Tabelle, zu der verschoben werden soll. |
| rowIndex | Int32 | Der Index der Zeile in der Tabelle. |
| columnIndex | Int32 | Der Index der Spalte in der Tabelle. |
| characterIndex | Int32 | Der Index des Zeichens innerhalb der Zelle. Mit einem negativen Wert können Sie eine Position vom Ende der Zelle angeben. Verwenden Sie -1, um zum Ende von der Zelle zu gelangen. |

### Bemerkungen

Die Navigation erfolgt innerhalb der aktuellen Geschichte des aktuellen Abschnitts.

Wenn Index größer oder gleich 0 ist, wird für die Indexparameter ein Index von am Anfang angegeben, wobei 0 das erste Element ist. Wenn der Index kleiner als 0 ist, wurde ein Index from the end angegeben, wobei -1 das letzte Element ist.

### Beispiele

Zeigt, wie der Cursor eines Document Builder zu einer Zelle in einer Tabelle bewegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine leere 2x2-Tabelle.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// Da wir die Tabelle mit der Methode EndTable beendet haben,
// Der Cursor des Dokumentenerstellers befindet sich derzeit außerhalb der Tabelle.
// Dieser Cursor hat dieselbe Funktion wie der blinkende Textcursor von Microsoft Word.
// Es kann auch mit den MoveTo-Methoden des Builders an eine andere Position im Dokument verschoben werden.
// Wir können den Cursor innerhalb der Tabelle zu einer bestimmten Zelle zurückbewegen.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)



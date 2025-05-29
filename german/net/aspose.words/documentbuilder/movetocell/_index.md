---
title: DocumentBuilder.MoveToCell
linktitle: MoveToCell
articleTitle: MoveToCell
second_title: Aspose.Words für .NET
description: Navigieren Sie mühelos durch Ihr Dokument mit der MoveToCell-Methode von DocumentBuilder und positionieren Sie den Cursor schnell in einer beliebigen Tabellenzelle, um die Bearbeitung zu verbessern.
type: docs
weight: 540
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
| characterIndex | Int32 | Der Index des Zeichens innerhalb der Zelle. Mit einem negativen Wert können Sie eine Position vom Ende der Zelle angeben. Verwenden Sie -1, um zum Ende der Zelle zu gelangen. |

## Bemerkungen

Die Navigation erfolgt innerhalb der aktuellen Story des aktuellen Abschnitts.

Wenn der Indexparameter größer oder gleich 0 ist, wird ein Index vom Anfang x000d angegeben, wobei 0 das erste Element ist. Wenn der Index kleiner als 0 ist, wird ein Index vom Ende x000 angegeben, wobei -1 das letzte Element ist.

## Beispiele

Zeigt, wie der Cursor eines Dokumentgenerators zu einer Zelle in einer Tabelle bewegt wird.

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
// Der Cursor des Dokumentgenerators befindet sich derzeit außerhalb der Tabelle.
// Dieser Cursor hat die gleiche Funktion wie der blinkende Textcursor von Microsoft Word.
// Es kann auch mit den MoveTo-Methoden des Builders an eine andere Stelle im Dokument verschoben werden.
// Wir können den Cursor innerhalb der Tabelle zurück zu einer bestimmten Zelle bewegen.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

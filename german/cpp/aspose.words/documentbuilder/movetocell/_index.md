---
title: "Aspose::Words::DocumentBuilder::MoveToCell Methode"
linktitle: "MoveToCell"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveToCell Methode. Verschiebt den Cursor zu einer Tabellenzelle im aktuellen Abschnitt in C++."
type: docs
weight: 53000
url: /de/cpp/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder::MoveToCell method


Bewegt den Cursor zu einer Tabellenzelle im aktuellen Abschnitt.

```cpp
void Aspose::Words::DocumentBuilder::MoveToCell(int32_t tableIndex, int32_t rowIndex, int32_t columnIndex, int32_t characterIndex)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableIndex | int32_t | Der Index der Tabelle, zu der bewegt werden soll. |
| rowIndex | int32_t | Der Index der Zeile in der Tabelle. |
| columnIndex | int32_t | Der Index der Spalte in der Tabelle. |
| characterIndex | int32_t | Der Index des Zeichens innerhalb der Zelle. Ein negativer Wert ermöglicht es, eine Position vom Ende der Zelle anzugeben. Verwenden Sie -1, um zum Ende der Zelle zu springen. |
## Hinweise


Die Navigation wird innerhalb der aktuellen Story des aktuellen Abschnitts durchgeführt.

Für die Indexparameter gibt ein Index, der größer oder gleich 0 ist, einen Index vom Anfang an an, wobei 0 das erste Element ist. Ist der Index kleiner als 0, gibt er einen Index vom Ende an, wobei -1 das letzte Element ist.

## Beispiele



Zeigt, wie der Cursor eines DocumentBuilder zu einer Zelle in einer Tabelle bewegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie eine leere 2 × 2‑Tabelle.
builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

// Da wir die Tabelle mit der EndTable‑Methode beendet haben,
// befindet sich der Cursor des DocumentBuilder derzeit außerhalb der Tabelle.
// Dieser Cursor hat dieselbe Funktion wie der blinkende Textcursor von Microsoft Word.
// Er kann auch mit den MoveTo‑Methoden des Builders an eine andere Stelle im Dokument verschoben werden.
// Wir können den Cursor zurück in die Tabelle zu einer bestimmten Zelle bewegen.
builder->MoveToCell(0, 1, 1, 0);
builder->Write(u"Column 2, cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MoveToCell.docx");
```

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

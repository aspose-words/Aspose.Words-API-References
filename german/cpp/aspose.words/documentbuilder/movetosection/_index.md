---
title: "Aspose::Words::DocumentBuilder::MoveToSection Methode"
linktitle: "MoveToSection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveToSection Methode. Verschiebt den Cursor zum Beginn des Body in einem angegebenen Abschnitt in C++."
type: docs
weight: 60000
url: /de/cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


Bewegt den Cursor zum Anfang des Hauptbereichs in einem angegebenen Abschnitt.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sectionIndex | int32_t | Der Index des Abschnitts, zu dem verschoben werden soll. |
## Hinweise


Wenn *sectionIndex* größer oder gleich 0 ist, gibt er einen Index vom Anfang des Dokuments an, wobei 0 den ersten Abschnitt bezeichnet. Wenn *sectionIndex* kleiner als 0 ist, gibt er einen Index vom Ende des Dokuments an, wobei -1 den letzten Abschnitt bezeichnet.

Der Cursor wird zum ersten Absatz im [Body](../../body/) des angegebenen Abschnitts verschoben.

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

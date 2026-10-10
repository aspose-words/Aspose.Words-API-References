---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class. Stellt eine Sammlung von Blasengrößen für eine Diagrammserie in C++ dar."
type: docs
weight: 3500
url: /de/cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


Stellt eine Sammlung von Blasengrößen für eine Diagrammreihe dar.

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Count](./get_count/)() | Gibt die Anzahl der Elemente in dieser Sammlung zurück. |
| [get_FormatCode](./get_formatcode/)() | Liest oder setzt den Formatcode, der auf die Blasengrößen angewendet wird. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Liest oder setzt den Blasengrößenwert am angegebenen Index. |
| [idx_set](./idx_set/)(int32_t, double) | Liest oder setzt den Blasengrößenwert am angegebenen Index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Setter für [Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Hinweise


Die Sammlung erlaubt nur das Ändern von Blasengrößen. Um neue Werte zu einer Diagrammserie hinzuzufügen oder einzufügen oder Werte zu entfernen, können die entsprechenden Methoden der Klasse [ChartSeries](../chartseries/) verwendet werden.

Leere Blasengrößenwerte werden als **NaN** dargestellt.

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)

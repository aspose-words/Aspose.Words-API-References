---
title: "Aspose::Words::Drawing::RelativeHorizontalSize enum"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::RelativeHorizontalSize enum. Gibt an, relativ zu was die Breite einer Form oder eines Textfelds horizontal in C++ berechnet wird."
type: docs
weight: 33500
url: /de/cpp/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enum


Gibt relativ dazu an, worauf die Breite einer Form oder eines Textfelds horizontal berechnet wird.

```cpp
enum class RelativeHorizontalSize
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Rand | 0 | Gibt an, dass die Breite relativ zum Abstand zwischen dem linken und dem rechten Rand berechnet wird. |
| Page | 1 | Gibt an, dass die Breite relativ zur Seitenbreite berechnet wird. |
| LeftMargin | 2 | Gibt an, dass die Breite relativ zur Größe des linken Randbereichs berechnet wird. |
| RightMargin | 3 | Gibt an, dass die Breite relativ zur Größe des rechten Randbereichs berechnet wird. |
| InnerMargin | 4 | Gibt an, dass die Breite relativ zur Größe des inneren Randbereichs berechnet wird, zur Größe des linken Randbereichs bei ungeraden Seiten und zur Größe des rechten Randbereichs bei geraden Seiten. |
| OuterMargin | 5 | Gibt an, dass die Breite relativ zur Größe des äußeren Randbereichs berechnet wird, zur Größe des rechten Randbereichs bei ungeraden Seiten und zur Größe des linken Randbereichs bei geraden Seiten. |
| Default | n/a | Standardwert ist [Margin](./). |


## Beispiele



Zeigt, wie man relative Größe und Position festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Hinzufügen einer einfachen Form mit absoluter Größe und Position.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// Setzen Sie WrapType auf WrapType.None, da Inline‑Formen automatisch in absolute Einheiten konvertiert werden.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Überprüfen und Festlegen der relativen horizontalen Größe.
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // Festlegen der Bindung der horizontalen Größe auf Margin.
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // Festlegen der Breite auf 50 % der Margin‑Breite.
    shape->set_WidthRelative(50.0f);
}

// Überprüfen und Festlegen der relativen vertikalen Größe.
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // Festlegen der Bindung der vertikalen Größe auf Margin.
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // Festlegen des heigh auf 30 % der Margin‑Höhe.
    shape->set_HeightRelative(30.0f);
}

// Überprüfen und Festlegen der relativen vertikalen Position.
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // Festlegen der Positionsbindung auf TopMargin.
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // Festlegen von Top relativ zu 30 % der TopMargin‑Position.
    shape->set_TopRelative(30.0f);
}

// Überprüfen und Festlegen der relativen horizontalen Position.
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // Festlegen der Positionsbindung auf RightMargin.
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // Der relative Positionswert kann negativ sein.
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

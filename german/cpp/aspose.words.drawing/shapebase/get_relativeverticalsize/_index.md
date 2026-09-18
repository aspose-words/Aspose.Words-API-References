---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize Methode"
linktitle: "get_RelativeVerticalSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize Methode. Liest oder setzt den Wert der relativen Größe der Form in vertikaler Richtung in C++."
type: docs
weight: 43500
url: /de/cpp/aspose.words.drawing/shapebase/get_relativeverticalsize/
---
## ShapeBase::get_RelativeVerticalSize method


Liest oder legt den Wert der relativen Größe der Form in vertikaler Richtung fest.

```cpp
Aspose::Words::Drawing::RelativeVerticalSize Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize()
```

## Hinweise


Der Standardwert ist [Margin](../../relativeverticalsize/).

Wirkt nur, wenn [HeightRelative](../get_heightrelative/) gesetzt ist.

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

* Enum [RelativeVerticalSize](../../relativeverticalsize/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

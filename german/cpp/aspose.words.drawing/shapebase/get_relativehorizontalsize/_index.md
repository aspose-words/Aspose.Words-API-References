---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize Methode"
linktitle: "get_RelativeHorizontalSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize Methode. Gibt den Wert der relativen Größe der Form in horizontaler Richtung zurück oder legt ihn fest in C++."
type: docs
weight: 42500
url: /de/cpp/aspose.words.drawing/shapebase/get_relativehorizontalsize/
---
## ShapeBase::get_RelativeHorizontalSize method


Liest oder legt den Wert der relativen Größe der Form in horizontaler Richtung fest.

```cpp
Aspose::Words::Drawing::RelativeHorizontalSize Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize()
```

## Hinweise


Der Standardwert ist [RelativeHorizontalSize](../../relativehorizontalsize/).

Wirkt nur, wenn [WidthRelative](../get_widthrelative/) gesetzt ist.

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

* Enum [RelativeHorizontalSize](../../relativehorizontalsize/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

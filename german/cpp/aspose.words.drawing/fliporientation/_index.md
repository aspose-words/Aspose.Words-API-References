---
title: "Aspose::Words::Drawing::FlipOrientation enum"
linktitle: "FlipOrientation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::FlipOrientation enum. Mögliche Werte für die Ausrichtung einer Form in C++."
type: docs
weight: 23000
url: /de/cpp/aspose.words.drawing/fliporientation/
---
## FlipOrientation enum


Mögliche Werte für die Ausrichtung einer Form.

```cpp
enum class FlipOrientation
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Koordinaten werden nicht gespiegelt. |
| Horizontal | 1 | Entlang der y-Achse spiegeln, wobei die x-Koordinaten umgekehrt werden. |
| Vertikal | 2 | Entlang der x-Achse spiegeln, wobei die y-Koordinaten umgekehrt werden. |
| Both | 3 | Entlang sowohl der y- als auch der x-Achse spiegeln. |


## Beispiele



Zeigt, wie man eine Form an einer Achse spiegelt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Bildform ein und belassen Sie ihre Ausrichtung im Standardzustand.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Setzen Sie die Eigenschaft "FlipOrientation" auf "FlipOrientation.Horizontal", um die zweite Form entlang der y-Achse zu spiegeln,
// und erzeugen ein horizontales Spiegelbild der ersten Form.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Setzen Sie die Eigenschaft "FlipOrientation" auf "FlipOrientation.Horizontal", um die dritte Form entlang der x-Achse zu spiegeln,
// und erzeugen ein vertikales Spiegelbild der ersten Form.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Setzen Sie die Eigenschaft "FlipOrientation" auf "FlipOrientation.Horizontal", um die vierte Form entlang beider Achsen, x und y, zu spiegeln,
// und erzeugen ein horizontales und vertikales Spiegelbild der ersten Form.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

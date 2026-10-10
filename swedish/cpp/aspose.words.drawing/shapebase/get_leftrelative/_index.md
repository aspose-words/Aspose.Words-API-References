---
title: "Aspose::Words::Drawing::ShapeBase::get_LeftRelative method"
linktitle: "get_LeftRelative"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_LeftRelative method. Hämtar eller anger värdet som representerar shape''s relativa vänstra position i procent i C++."
type: docs
weight: 38500
url: /sv/cpp/aspose.words.drawing/shapebase/get_leftrelative/
---
## ShapeBase::get_LeftRelative method


Hämtar eller anger värdet som representerar formens relativa vänstra position i procent.

```cpp
float Aspose::Words::Drawing::ShapeBase::get_LeftRelative()
```


## Exempel



Visar hur man ställer in relativ storlek och position.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägger till en enkel form med absolut storlek och position.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// Ställ in WrapType till WrapType.None eftersom Inline-former automatiskt konverteras till absoluta enheter.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Kontrollerar och ställer in den relativa horisontella storleken.
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // Ställer in den horisontella storleksbindningen till Margin.
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // Ställer in bredden till 50 % av Margins bredd.
    shape->set_WidthRelative(50.0f);
}

// Kontrollerar och ställer in den relativa vertikala storleken.
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // Ställer in den vertikala storleksbindningen till Margin.
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // Ställer in höjden till 30 % av Margins höjd.
    shape->set_HeightRelative(30.0f);
}

// Kontrollerar och ställer in den relativa vertikala positionen.
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // Ställer in positionsbindningen till TopMargin.
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // Ställer in relativ Top till 30 % av TopMargin-positionen.
    shape->set_TopRelative(30.0f);
}

// Kontrollerar och ställer in den relativa horisontella positionen.
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // Ställer in positionsbindningen till RightMargin.
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // Det relativa positionsvärdet kan vara negativt.
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

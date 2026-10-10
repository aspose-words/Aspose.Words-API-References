---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize metod"
linktitle: "get_RelativeVerticalSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize metod. Hämtar eller anger värdet för formens relativa storlek i vertikal riktning i C++."
type: docs
weight: 43500
url: /sv/cpp/aspose.words.drawing/shapebase/get_relativeverticalsize/
---
## ShapeBase::get_RelativeVerticalSize method


Hämtar eller anger värdet för formens relativa storlek i vertikal riktning.

```cpp
Aspose::Words::Drawing::RelativeVerticalSize Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize()
```

## Anmärkningar


Standardvärdet är [Margin](../../relativeverticalsize/).

Har endast effekt om [HeightRelative](../get_heightrelative/) är angivet.

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

* Enum [RelativeVerticalSize](../../relativeverticalsize/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

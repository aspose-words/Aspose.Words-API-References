---
title: "Aspose::Words::Drawing::RelativeHorizontalSize enum"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::RelativeHorizontalSize enum. Anger relativt till vad bredden på en form eller en textram beräknas horisontellt i C++."
type: docs
weight: 33500
url: /sv/cpp/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enum


Anger relativt vad bredden på en form eller en textruta beräknas horisontellt.

```cpp
enum class RelativeHorizontalSize
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Marginal | 0 | Anger att bredden beräknas relativt till utrymmet mellan vänster- och högermarginalen. |
| Page | 1 | Anger att bredden beräknas relativt till sidbredden. |
| LeftMargin | 2 | Anger att bredden beräknas relativt till storleken på vänstermarginalområdet. |
| RightMargin | 3 | Anger att bredden beräknas relativt till storleken på högermarginalområdet. |
| InnerMargin | 4 | Anger att bredden beräknas relativt till det inre marginalområdet, till vänstermarginalområdet för udda sidor och till högermarginalområdet för jämna sidor. |
| OuterMargin | 5 | Anger att bredden beräknas relativt till det yttre marginalområdet, till högermarginalområdet för udda sidor och till vänstermarginalområdet för jämna sidor. |
| Default | n/a | Standardvärdet är [Margin](./). |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

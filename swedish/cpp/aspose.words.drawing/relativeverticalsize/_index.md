---
title: "Aspose::Words::Drawing::RelativeVerticalSize enum"
linktitle: "RelativeVerticalSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::RelativeVerticalSize enum. Anger relativt till vad höjden på en form eller en textram beräknas vertikalt i C++."
type: docs
weight: 34500
url: /sv/cpp/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enum


Anger relativt vad höjden på en form eller en textruta beräknas vertikalt.

```cpp
enum class RelativeVerticalSize
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Marginal | 0 | Anger att höjden beräknas relativt till utrymmet mellan den övre och den nedre marginalen. |
| Page | 1 | Anger att höjden beräknas relativt till sidans höjd. |
| TopMargin | 2 | Anger att höjden beräknas relativt till storleken på det övre marginalområdet. |
| BottomMargin | 3 | Anger att höjden beräknas relativt till storleken på det nedre marginalområdet. |
| InnerMargin | 4 | Anger att höjden beräknas relativt till storleken på det inre marginalområdet, till det övre marginalområdet för udda sidor och till det nedre marginalområdet för jämna sidor. |
| OuterMargin | 5 | Anger att höjden beräknas relativt till storleken på det yttre marginalområdet, till det nedre marginalområdet för udda sidor och till det övre marginalområdet för jämna sidor. |
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

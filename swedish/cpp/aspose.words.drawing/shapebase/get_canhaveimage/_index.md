---
title: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage metod"
linktitle: "get_CanHaveImage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage metod. Returnerar **true** om shapetypen tillåter att formen har en bild i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


Returnerar **true** om formtypen tillåter att formen har en bild.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## Anmärkningar


Även om Microsoft Word har en speciell shapetyp för bilder, verkar det som att i Microsoft Word-dokument kan alla former förutom en gruppform ha en bild, därför returnerar den här egenskapen **true** för alla former förutom [GroupShape](../../groupshape/).

## Exempel



Visar hur man infogar och roterar en bild.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en form med en bild.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Rotera bilden 45 grader medurs.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

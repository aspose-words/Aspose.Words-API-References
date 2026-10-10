---
title: "Aspose::Words::Drawing::ShapeBase::get_Rotation metod"
linktitle: "get_Rotation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Rotation metod. Definierar vinkeln (i grader) som en form roteras. Positivt värde motsvarar medurs rotationsvinkel i C++."
type: docs
weight: 45000
url: /sv/cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


Definierar vinkeln (i grader) som en form roteras. Positivt värde motsvarar medurs rotationsvinkel.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## Anmärkningar


Standardvärdet är 0.

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

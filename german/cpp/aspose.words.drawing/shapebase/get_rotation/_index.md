---
title: "Aspose::Words::Drawing::ShapeBase::get_Rotation Methode"
linktitle: "get_Rotation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_Rotation Methode. Definiert den Winkel (in Grad), um den eine Form gedreht wird. Ein positiver Wert entspricht einem im Uhrzeigersinn gedrehten Winkel in C++."
type: docs
weight: 45000
url: /de/cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


Definiert den Winkel (in Grad), um den eine Form gedreht wird. Ein positiver Wert entspricht einem im Uhrzeigersinn gedrehten Winkel.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## Hinweise


Der Standardwert ist 0.

## Beispiele



Zeigt, wie man ein Bild einfügt und rotiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Füge eine Form mit einem Bild ein.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Rotiere das Bild um 45 Grad im Uhrzeigersinn.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

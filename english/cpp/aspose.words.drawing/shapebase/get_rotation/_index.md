---
title: Aspose::Words::Drawing::ShapeBase::get_Rotation method
linktitle: get_Rotation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_Rotation method. Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle in C++.'
type: docs
weight: 45000
url: /cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## Remarks


The default value is 0.

## Examples



Shows how to insert and rotate an image. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a shape with an image.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Rotate the image 45 degrees clockwise.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

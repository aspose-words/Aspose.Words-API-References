---
title: Aspose::Words::Drawing::ShapeBase::get_CanHaveImage method
linktitle: get_CanHaveImage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_CanHaveImage method. Returns true if the shape type allows the shape to have an image in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


Returns **true** if the shape type allows the shape to have an image.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## Remarks


Although Microsoft Word has a special shape type for images, it appears that in Microsoft Word documents any shape except a group shape can have an image, therefore this property returns **true** for all shapes except [GroupShape](../../groupshape/).

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

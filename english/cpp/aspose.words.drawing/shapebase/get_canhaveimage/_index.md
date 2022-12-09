---
title: get_CanHaveImage
second_title: Aspose.Words for C++ API Reference
description: Returns true if the shape type allows the shape to have an image.
type: docs
weight: 144
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a shape with an image.
SharedPtr<Shape> shape = builder->InsertImage(System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg"));
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Rotate the image 45 degrees clockwise.
shape->set_Rotation(45);

doc->Save(ArtifactsDir + u"Shape.Rotate.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)

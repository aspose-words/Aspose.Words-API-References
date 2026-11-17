---
title: Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked method
linktitle: get_AspectRatioLocked
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked method. Specifies whether the shape''s aspect ratio is locked in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


Specifies whether the shape's aspect ratio is locked.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## Remarks


The default value depends on the [ShapeType](../../shapetype/), for the [Image](../../shapetype/) it is **true** but for the other shape types it is **false**.

Has effect for top level shapes only.

## Examples



Shows how to lock/unlock a shape's aspect ratio. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a shape. If we open this document in Microsoft Word, we can left click the shape to reveal
// eight sizing handles around its perimeter, which we can click and drag to change its size.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Set the "AspectRatioLocked" property to "true" to preserve the shape's aspect ratio
// when using any of the four diagonal sizing handles, which change both the image's height and width.
// Using any orthogonal sizing handles that either change the height or width will still change the aspect ratio.
// Set the "AspectRatioLocked" property to "false" to allow us to
// freely change the image's aspect ratio with all sizing handles.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

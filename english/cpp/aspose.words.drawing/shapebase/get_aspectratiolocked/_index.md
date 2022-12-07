---
title: get_AspectRatioLocked
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the shape's aspect ratio is locked.
type: docs
weight: 66
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a shape. If we open this document in Microsoft Word, we can left click the shape to reveal
// eight sizing handles around its perimeter, which we can click and drag to change its size.
SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Logo.jpg");

// Set the "AspectRatioLocked" property to "true" to preserve the shape's aspect ratio
// when using any of the four diagonal sizing handles, which change both the image's height and width.
// Using any orthogonal sizing handles that either change the height or width will still change the aspect ratio.
// Set the "AspectRatioLocked" property to "false" to allow us to
// freely change the image's aspect ratio with all sizing handles.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(ArtifactsDir + u"Shape.AspectRatio.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)

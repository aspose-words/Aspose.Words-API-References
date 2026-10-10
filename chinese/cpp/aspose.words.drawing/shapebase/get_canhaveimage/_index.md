---
title: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage 方法"
linktitle: "get_CanHaveImage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage 方法。如果形状类型允许形状拥有图像，则在 C++ 中返回 **true**。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


如果形状类型允许形状具有图像，则返回 **true**。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## 备注


虽然 Microsoft Word 为图像提供了特殊的形状类型，但在 Microsoft Word 文档中，除组形状外的任何形状都可以包含图像，因此此属性对除 [GroupShape](../../groupshape/) 之外的所有形状返回 **true**。

## 示例



展示如何插入和旋转图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入带有图像的形状。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// 将图像顺时针旋转 45 度。
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

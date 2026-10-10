---
title: "Aspose::Words::Drawing::ShapeBase::get_Rotation 方法"
linktitle: "get_Rotation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_Rotation 方法。定义形状旋转的角度（以度为单位）。正值对应顺时针旋转角度（C++）。"
type: docs
weight: 45000
url: /zh/cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


定义形状旋转的角度（以度为单位）。正值对应顺时针旋转角度。

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## 备注


默认值为 0。

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

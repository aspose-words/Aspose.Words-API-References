---
title: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked 方法"
linktitle: "get_AspectRatioLocked"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked 方法。指定在 C++ 中形状的宽高比是否被锁定。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


指定形状的宽高比是否被锁定。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## 备注


默认值取决于 [ShapeType](../../shapetype/)，对于 [Image](../../shapetype/) 为 **true**，而对于其他形状类型为 **false**。

仅对顶层形状有效。

## 示例



演示如何锁定/解锁形状的宽高比。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个形状。如果我们在 Microsoft Word 中打开此文档，可以左键单击该形状以显示
// 其周围的八个尺寸控制点，我们可以点击并拖动以改变其大小。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 将 "AspectRatioLocked" 属性设置为 "true" 以保持形状的宽高比
// 当使用四个对角尺寸控制点时，它们会同时改变图像的高度和宽度。
// 使用任何垂直或水平的尺寸控制点（仅改变高度或宽度）仍会改变宽高比。
// 将 "AspectRatioLocked" 属性设置为 "false" 以允许我们
// 使用所有尺寸控制点自由改变图像的宽高比。
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

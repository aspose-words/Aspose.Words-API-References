---
title: "Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment 方法"
linktitle: "get_VerticalAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment 方法。指定形状在 C++ 中的垂直定位方式。"
type: docs
weight: 53000
url: /zh/cpp/aspose.words.drawing/shapebase/get_verticalalignment/
---
## ShapeBase::get_VerticalAlignment method


指定形状在垂直方向上的定位方式。

```cpp
Aspose::Words::Drawing::VerticalAlignment Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment()
```

## 备注


默认值是 [None](../../verticalalignment/)。

仅对顶层浮动形状有效。

## 示例



展示如何在页面中心插入浮动图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个浮动图像，使其出现在重叠文本后面，并将其对齐到页面中心。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## 另见

* Enum [VerticalAlignment](../../verticalalignment/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

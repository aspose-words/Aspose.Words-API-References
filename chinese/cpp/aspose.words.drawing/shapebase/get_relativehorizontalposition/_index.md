---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition 方法"
linktitle: "get_RelativeHorizontalPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition 方法。指定形状在 C++ 中水平定位相对于什么。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words.drawing/shapebase/get_relativehorizontalposition/
---
## ShapeBase::get_RelativeHorizontalPosition method


指定形状在水平方向上相对于何物进行定位。

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition()
```

## 备注


默认值是 [Column](../../relativehorizontalposition/)。

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

* Enum [RelativeHorizontalPosition](../../relativehorizontalposition/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

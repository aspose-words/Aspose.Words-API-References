---
title: "Aspose::Words::Drawing::ShapeBase::get_DistanceTop method"
linktitle: "get_DistanceTop"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_DistanceTop 方法。返回或设置 C++ 中文档文本与形状顶部边缘之间的距离（以点为单位）。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.drawing/shapebase/get_distancetop/
---
## ShapeBase::get_DistanceTop method


返回或设置文档文本与形状顶部边缘之间的距离（单位为点）。

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceTop()
```

## 备注


默认值为 0。

仅对顶层形状有效。

## 示例



展示如何设置环绕形状的文本的包装距离。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个矩形，并使文本紧贴其边界换行。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 150, 150);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Tight);

// 将形状与周围文本之间的最小距离设置为四周 40pt。
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// 将形状移动更靠近页面中心，然后顺时针旋转形状 60 度。
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// 添加环绕形状的文本。
builder->get_Font()->set_Size(24);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"Shape.Coordinates.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

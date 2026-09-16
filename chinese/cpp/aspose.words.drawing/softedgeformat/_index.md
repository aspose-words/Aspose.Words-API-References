---
title: "Aspose::Words::Drawing::SoftEdgeFormat 类"
linktitle: "SoftEdgeFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::SoftEdgeFormat 类。表示 C++ 中对象的软边缘格式。"
type: docs
weight: 13500
url: /zh/cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


表示对象的柔和边缘格式。

```cpp
class SoftEdgeFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Radius](./get_radius/)() | 获取或设置一个 double 值，表示软边缘效果的半径长度，单位为点 (pt)。默认值为 0.0。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | 从父对象中移除 [SoftEdgeFormat](./)。 |
| [set_Radius](./set_radius/)(double) | 用于 [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/) 的设置器。 |
| static [Type](./type/)() |  |
## 备注


使用 [SoftEdge](../shapebase/get_softedge/) 属性来访问对象的软边缘属性。您不能直接创建 [SoftEdgeFormat](./) 类的实例。

## 示例



展示如何使用软边缘格式。
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// 将软边缘应用于形状。
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// 加载包含软边缘矩形形状的文档。
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// 检查软边缘半径。
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// 从形状中移除软边缘。
softEdgeFormat->Remove();

// 检查已移除软边缘的半径。
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

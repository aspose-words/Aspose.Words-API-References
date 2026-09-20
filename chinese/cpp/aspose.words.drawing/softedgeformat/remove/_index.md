---
title: "Aspose::Words::Drawing::SoftEdgeFormat::Remove 方法"
linktitle: "Remove"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::SoftEdgeFormat::Remove 方法。 在 C++ 中从父对象中移除 SoftEdgeFormat。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat::Remove method


从父对象中移除 [SoftEdgeFormat](../)。

```cpp
void Aspose::Words::Drawing::SoftEdgeFormat::Remove()
```


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


展示如何设置图像分辨率的限制。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## 另见

* Class [SoftEdgeFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

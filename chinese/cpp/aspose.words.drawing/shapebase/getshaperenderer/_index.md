---
title: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer 方法"
linktitle: "GetShapeRenderer"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer 方法。创建并返回一个可用于在 C++ 中将此形状渲染为图像的对象。"
type: docs
weight: 58000
url: /zh/cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


创建并返回一个可用于将此形状渲染为图像的对象。

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

此形状的渲染器对象。
## 备注


此方法仅调用 [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) 构造函数，并将此对象作为参数传递。

## 示例



展示如何使用形状渲染器将形状导出到本地文件系统中的文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// 文档中有 7 个形状，包括一个包含 2 个子形状的组合形状。
// 我们将在本地文件系统中将每个形状渲染为图像文件
// 同时忽略组合形状，因为它们没有外观。
// 这将生成 6 个图像文件。
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## 另见

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

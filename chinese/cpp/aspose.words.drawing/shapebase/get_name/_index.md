---
title: "Aspose::Words::Drawing::ShapeBase::get_Name method"
linktitle: "get_Name"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_Name 方法。获取或设置 C++ 中的可选形状名称。"
type: docs
weight: 40000
url: /zh/cpp/aspose.words.drawing/shapebase/get_name/
---
## ShapeBase::get_Name method


获取或设置可选的形状名称。

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Name()
```

## 备注


默认是空字符串。

不能为 **null**，但可以是空字符串。

## 示例



展示如何使用形状的替代文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// 我们可以通过右键单击形状，然后通过 \"Format AutoShape\" -> \"Alt Text\" 来访问形状的替代文本。
doc->Save(get_ArtifactsDir() + u"Shape.AltText.docx");

// 将文档保存为 HTML，然后删除属于我们形状的链接图像。
// 读取我们 HTML 的浏览器将在缺失图像的位置显示替代文本。
doc->Save(get_ArtifactsDir() + u"Shape.AltText.html");
System::IO::File::Delete(get_ArtifactsDir() + u"Shape.AltText.001.png");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

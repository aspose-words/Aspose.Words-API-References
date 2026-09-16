---
title: "Aspose::Words::Drawing::ShapeBase::get_Title 方法"
linktitle: "get_Title"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_Title 方法。获取或设置当前形状对象的标题（说明）（C++）。"
type: docs
weight: 51000
url: /zh/cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


获取或设置当前形状对象的标题（说明）。

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## 备注


默认是空字符串。

不能为 **null**，但可以是空字符串。

## 示例



展示如何设置形状的标题。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个形状，为其设置标题，然后将其添加到文档中。
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// 当我们保存一个带有标题的形状的文档时，
// Aspose.Words 会将该标题存储在形状的 Alt Text 中。
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

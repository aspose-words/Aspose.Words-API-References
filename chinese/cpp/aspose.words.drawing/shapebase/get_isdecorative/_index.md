---
title: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative 方法"
linktitle: "get_IsDecorative"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative 方法。获取或设置一个标志，指定该形状在文档中是否为装饰性形状（在 C++ 中）。"
type: docs
weight: 25000
url: /zh/cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


获取或设置指定形状在文档中是否为装饰性的标志。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## 示例



展示如何设置形状为装饰性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// 如果 "AlternativeText" 不为空，则形状不能是装饰性的。
// 这就是我们的值已更改为 'false' 的原因。
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// 创建一个装饰性的形状。
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

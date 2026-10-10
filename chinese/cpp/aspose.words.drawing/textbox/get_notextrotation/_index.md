---
title: "Aspose::Words::Drawing::TextBox::get_NoTextRotation 方法"
linktitle: "get_NoTextRotation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::TextBox::get_NoTextRotation 方法。获取或设置一个布尔值，指示 TextBox 的文本在形状旋转时是否不旋转（在 C++ 中）。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


获取或设置一个布尔值，指示 [TextBox](../) 的文本在形状旋转时是否不旋转。

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## 备注


默认值为 **false**

## 示例



展示如何在形状旋转时禁用文本旋转。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## 另见

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

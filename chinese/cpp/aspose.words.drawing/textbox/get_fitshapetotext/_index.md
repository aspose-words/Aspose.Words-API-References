---
title: "Aspose::Words::Drawing::TextBox::get_FitShapeToText 方法"
linktitle: "get_FitShapeToText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::TextBox::get_FitShapeToText 方法。确定 Microsoft Word 在 C++ 中是否会扩展形状以适应文本。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


确定 Microsoft Word 是否会扩大形状以适应文本。

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## 备注


默认值为 **false**。

## 示例



展示如何让文本框自行调整大小以紧密适应其内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// 将这些值应用于这两个成员，以使父形状适应
// 紧贴文本内容，忽略我们设置的尺寸。
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## 另见

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

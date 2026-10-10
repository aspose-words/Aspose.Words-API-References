---
title: "Aspose::Words::Drawing::TextBox::get_InternalMarginLeft 方法"
linktitle: "get_InternalMarginLeft"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::TextBox::get_InternalMarginLeft 方法。指定形状在 C++ 中的内部左边距（以点为单位）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.drawing/textbox/get_internalmarginleft/
---
## TextBox::get_InternalMarginLeft method


指定形状的内部左侧边距（单位：磅）。

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginLeft()
```

## 备注


默认值为 1/10 英寸。

## 示例



展示如何为文本框设置内部边距。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入另一个具有特定边距的文本框。
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## 另见

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

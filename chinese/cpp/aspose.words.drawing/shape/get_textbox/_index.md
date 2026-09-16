---
title: "Aspose::Words::Drawing::Shape::get_TextBox 方法"
linktitle: "get_TextBox"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Shape::get_TextBox 方法。定义在 C++ 中指定文本在形状中如何显示的属性。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


定义指定文本在形状中显示方式的属性。

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
```


## 示例



展示如何设置文本框内文本的方向。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// 将文档生成器移动到 TextBox 内部并添加文本。
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// 设置 "LayoutFlow" 属性，以为此文本框的文本内容设定方向。
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## 另见

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

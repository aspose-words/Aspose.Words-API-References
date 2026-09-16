---
title: "Aspose::Words::Drawing::TextBox class"
linktitle: "文本框"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::TextBox 类。定义指定文本在形状内部如何显示的属性。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.drawing/textbox/
---
## TextBox class


定义指定文本在形状内部显示方式的属性。要了解更多信息，请访问 [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) 文档文章。

```cpp
class TextBox : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | 中断到下一个 [TextBox](./) 的链接。 |
| [get_FitShapeToText](./get_fitshapetotext/)() | 确定 Microsoft Word 是否会扩大形状以适应文本。 |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | 指定形状的内部底部边距（单位：磅）。 |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | 指定形状的内部左侧边距（单位：磅）。 |
| [get_InternalMarginRight](./get_internalmarginright/)() | 指定形状的内部右侧边距（单位：磅）。 |
| [get_InternalMarginTop](./get_internalmargintop/)() | 指定形状的内部顶部边距（单位：磅）。 |
| [get_LayoutFlow](./get_layoutflow/)() | 确定文本在形状中的布局流向。 |
| [get_Next](./get_next/)() | 返回或设置一个表示形状序列中下一个 [TextBox](./) 的 [TextBox](./)。 |
| [get_NoTextRotation](./get_notextrotation/)() | 获取或设置一个布尔值，指示当形状旋转时，[TextBox](./) 的文本是否不应旋转。 |
| [get_Parent](./get_parent/)() const | 获取 [TextBox](./) 的父形状。 |
| [get_Previous](./get_previous/)() | 返回一个表示形状序列中上一个 [TextBox](./) 的 [TextBox](./)。 |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | 确定文本在形状内部的换行方式。 |
| [get_VerticalAnchor](./get_verticalanchor/)() | 指定文本在形状内部的垂直对齐方式。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | 确定此 [TextBox](./) 是否可以链接到目标 [TextBox](./)。 |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | 用于 [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/) 的 setter。 |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | 用于 [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/) 的 setter。 |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | 用于 [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/) 的 setter。 |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | 用于 [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/) 的 setter。 |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | 用于 [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/) 的 setter。 |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | 用于 [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/) 的 setter。 |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | 用于 [Aspose::Words::Drawing::TextBox::get_Next](./get_next/) 的 setter。 |
| [set_NoTextRotation](./set_notextrotation/)(bool) | 用于 [Aspose::Words::Drawing::TextBox::get_NoTextRotation](./get_notextrotation/) 的 setter。 |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | 用于 [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/) 的 setter。 |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | 用于 [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


使用 [TextBox](../shape/get_textbox/) 属性来访问形状的文本属性。您不能直接创建 [TextBox](./) 类的实例。

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

---
title: "Aspose::Words::Drawing::Shape::Shape 构造函数"
linktitle: "形状"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Shape::Shape 构造函数。创建一个新的形状对象（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


创建一个新的形状对象。

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 所属文档。 |
| shapeType | Aspose::Words::Drawing::ShapeType | 要创建的形状类型。 |
## 备注


在创建形状后，您应该指定所需的形状属性。

## 示例



展示如何将本地文件系统中的图像插入为形状到文档中。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// "Shape" 类的公共构造函数将创建一个使用 "ShapeMarkupLanguage.Vml" 标记类型的形状。
// 如果需要创建非原始类型的形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
// TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded，
// 请使用 DocumentBuilder.InsertShape。
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


展示如何创建和格式化文本框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建一个浮动文本框。
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// 设置形状内部文本的水平和垂直对齐方式。
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// 向文本框添加段落，并添加文本运行，以便文本框显示。
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## 另见

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

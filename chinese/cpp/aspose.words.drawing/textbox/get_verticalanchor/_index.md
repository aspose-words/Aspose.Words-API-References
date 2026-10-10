---
title: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor 方法"
linktitle: "get_VerticalAnchor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor 方法。指定文本在 C++ 中形状内部的垂直对齐方式。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


指定文本在形状内部的垂直对齐方式。

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## 备注


默认值为 [Top](../../textboxanchor/)。

## 示例



展示如何垂直对齐文本框的文本内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// 将 "VerticalAnchor" 属性设置为 "TextBoxAnchor.Top" 以
// 使此文本框中的文本与形状的顶部对齐。
// 将 "VerticalAnchor" 属性设置为 "TextBoxAnchor.Middle" 以
// 使此文本框中的文本居中于形状。
// 将 "VerticalAnchor" 属性设置为 "TextBoxAnchor.Bottom" 以
// 使此文本框中的文本与形状的底部对齐。
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// 从 Microsoft Word 2007 起，文本框内文本的垂直对齐功能可用。
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## 另见

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

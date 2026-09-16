---
title: "Aspose::Words::Drawing::TextBoxAnchor enum"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::TextBoxAnchor enum. 指定在 C++ 中用于形状文本垂直对齐的值。"
type: docs
weight: 39000
url: /zh/cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


指定用于形状文本垂直对齐的值。

```cpp
enum class TextBoxAnchor
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 顶部 | 0 | 文本对齐到文本框的顶部。 |
| 居中 | 1 | 文本对齐到文本框的中部。 |
| 底部 | 2 | 文本对齐到文本框的底部。 |
| 顶部居中 | 3 | 文本对齐到文本框的顶部居中。 |
| 中部居中 | 4 | 文本对齐到文本框的中部居中。 |
| 底部居中 | 5 | 文本对齐到文本框的底部居中。 |
| 顶部基线 | 6 | 文本对齐到文本框的顶部基线。 |
| 底部基线 | 7 | 文本对齐到文本框的底部基线。 |
| 顶部居中基线 | 8 | 文本对齐到文本框的顶部居中基线。 |
| 底部居中基线 | 9 | 文本对齐到文本框的底部居中基线。 |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

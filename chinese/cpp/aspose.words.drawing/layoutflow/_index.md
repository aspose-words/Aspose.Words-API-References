---
title: "Aspose::Words::Drawing::LayoutFlow 枚举"
linktitle: "LayoutFlow"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::LayoutFlow 枚举。确定 C++ 中文本框中文本布局的流向。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


确定文本框中文本布局的流向。

```cpp
enum class LayoutFlow
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Horizontal | 0 | 文本水平显示。 |
| TopToBottomIdeographic | 1 | 表意文字垂直显示。 |
| BottomToTop | 2 | 文本垂直显示。 |
| TopToBottom | 3 | 文本垂直显示。 |
| HorizontalIdeographic | 4 | 表意文字水平显示。 |
| Vertical | 5 | 文本垂直显示。 |


## 示例



展示如何向文本框添加文本并更改其方向
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto textbox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textbox->set_Width(100);
textbox->set_Height(100);
textbox->get_TextBox()->set_LayoutFlow(Aspose::Words::Drawing::LayoutFlow::BottomToTop);

textbox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
builder->InsertNode(textbox);

builder->MoveTo(textbox->get_FirstParagraph());
builder->Write(u"This text is flipped 90 degrees to the left.");

doc->Save(get_ArtifactsDir() + u"Drawing.TextBox.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

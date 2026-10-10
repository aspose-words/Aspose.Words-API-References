---
title: "Aspose::Words::ParagraphFormat::get_WidowControl 方法"
linktitle: "get_WidowControl"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_WidowControl 方法。如果段落的首行和末行应与段落其余部分保持在同一页，则返回 true，适用于 C++。"
type: docs
weight: 41000
url: /zh/cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


如果段落的第一行和最后一行应与段落其余部分保持在同一页，则为 True。

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## 示例



展示如何为段落启用寡妇/孤儿控制。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 当我们编写的文本无法容纳在一页时，可能会有一行溢出到下一页。
// 出现在下一页的单行称为"Orphan"，
// 而导致孤儿断开的前一行称为"Widow"。
// 我们可以通过调整字体大小、间距或页面边距来修复孤行和寡行。
// 如果我们希望保留文档的尺寸，可以将此标志设置为 "true"
// 将寡行推到与其对应的孤行同一页上。
// 将此标志保持为 "false" 将在文本中保留寡行/孤行对。
// 每个段落都有此设置，可在 Microsoft Word 中通过 首页 -> 段落 -> 段落设置 访问。
// (位于 "Paragraph" 选项卡右下角的按钮) -> "Widow/Orphan control"。
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// 插入会产生孤行和寡行的文本。
builder->get_Font()->set_Size(68);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.WidowControl.docx");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

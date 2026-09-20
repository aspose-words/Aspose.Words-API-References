---
title: "Aspose::Words::Font::get_StrikeThrough 方法"
linktitle: "get_StrikeThrough"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_StrikeThrough 方法。若在 C++ 中字体被设置为删除线格式，则为 True。"
type: docs
weight: 41000
url: /zh/cpp/aspose.words/font/get_strikethrough/
---
## Font::get_StrikeThrough method


如果字体被格式化为删除线文本，则为 True。

```cpp
bool Aspose::Words::Font::get_StrikeThrough()
```


## 示例



展示如何为文本添加删除线。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a single-line strikethrough.");
run->get_Font()->set_StrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a double-line strikethrough.");
run->get_Font()->set_DoubleStrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.StrikeThrough.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Font::get_DoubleStrikeThrough 方法"
linktitle: "get_DoubleStrikeThrough"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_DoubleStrikeThrough 方法。如果字体在 C++ 中被格式化为双删除线文本，则为 true。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/font/get_doublestrikethrough/
---
## Font::get_DoubleStrikeThrough method


如果字体格式为双删除线文本，则为 True。

```cpp
bool Aspose::Words::Font::get_DoubleStrikeThrough()
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

---
title: "Aspose::Words::Font::get_Position 方法"
linktitle: "get_Position"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Position 方法。获取或设置文本相对于基线的位置（以点为单位）。正数会提升文本，负数会降低文本，在 C++ 中。"
type: docs
weight: 32000
url: /zh/cpp/aspose.words/font/get_position/
---
## Font::get_Position method


获取或设置文本相对于基线的位置（以磅为单位）。正数会提升文本，负数会降低文本。

```cpp
double Aspose::Words::Font::get_Position()
```


## 示例



展示如何格式化文本以偏移其位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// 将此文本段提升 5 点至基线之上。
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// 将此文本段降低 10 点至基线之下。
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// 添加一段普通文本。
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// 添加一段以下标形式显示的文本。
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// 添加一段以上标形式显示的文本。
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

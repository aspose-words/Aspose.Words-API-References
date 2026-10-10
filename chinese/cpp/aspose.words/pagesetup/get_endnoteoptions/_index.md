---
title: "Aspose::Words::PageSetup::get_EndnoteOptions 方法"
linktitle: "get_EndnoteOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_EndnoteOptions 方法。提供在 C++ 中控制本节尾注编号和位置的选项。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/pagesetup/get_endnoteoptions/
---
## PageSetup::get_EndnoteOptions method


提供控制本节尾注编号和位置的选项。

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::PageSetup::get_EndnoteOptions()
```


## 示例



展示如何配置影响章节中脚注/尾注的选项。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// 将第一节中的所有脚注配置为从 1 重新开始编号
// 在每个新页面上，并在每页的文本下方直接显示它们。
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// 将第一节中的所有尾注配置为在整个章节中保持连续计数，
// 从 1 开始。此外，将它们全部设置为在文档末尾集中显示。
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## 另见

* Class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::PageSetup::get_RestartPageNumbering 方法"
linktitle: "get_RestartPageNumbering"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_RestartPageNumbering 方法。如果页码在 C++ 中于章节开头重新开始，则为 true。"
type: docs
weight: 38000
url: /zh/cpp/aspose.words/pagesetup/get_restartpagenumbering/
---
## PageSetup::get_RestartPageNumbering method


如果页码在章节开头重新开始，则为 true。

```cpp
bool Aspose::Words::PageSetup::get_RestartPageNumbering()
```


## 示例



展示如何在章节中设置页码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// 将文档构建器移动到第一章节的主页眉，
// 该章节的每一页都会显示此页眉。
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// 插入一个 PAGE 域，它将显示当前页的页码。
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// 配置章节，使 PAGE 域显示的页码从 5 开始计数。
// 此外，配置所有 PAGE 域使用大写罗马数字显示页码。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// 为第二章节创建另一个主页眉，并包含另一个 PAGE 域。
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// 配置章节，使 PAGE 域显示的页码从 10 开始计数。
// 此外，配置所有 PAGE 域使用阿拉伯数字显示页码。
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

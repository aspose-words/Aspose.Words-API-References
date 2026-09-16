---
title: "Aspose::Words::Document::get_Sections 方法"
linktitle: "get_Sections"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_Sections 方法。返回一个集合，表示 C++ 中文档的所有节。"
type: docs
weight: 48000
url: /zh/cpp/aspose.words/document/get_sections/
---
## Document::get_Sections method


返回表示文档中所有章节的集合。

```cpp
System::SharedPtr<Aspose::Words::SectionCollection> Aspose::Words::Document::get_Sections()
```


## 示例



展示如何指定新章节与前一章节的分隔方式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"This text is in section 1.");

// 分节符类型决定新章节与前一章节的分隔方式。
// 以下是五种分节符类型。
// 1 -  在新页上开始下一章节：
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"This text is in section 2.");

ASSERT_EQ(Aspose::Words::SectionStart::NewPage, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());

// 2 -  在当前页上开始下一章节：
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"This text is in section 3.");

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, doc->get_Sections()->idx_get(2)->get_PageSetup()->get_SectionStart());

// 3 -  在新偶数页上开始下一章节：
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Writeln(u"This text is in section 4.");

ASSERT_EQ(Aspose::Words::SectionStart::EvenPage, doc->get_Sections()->idx_get(3)->get_PageSetup()->get_SectionStart());

// 4 -  在新奇数页上开始下一章节：
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakOddPage);
builder->Writeln(u"This text is in section 5.");

ASSERT_EQ(Aspose::Words::SectionStart::OddPage, doc->get_Sections()->idx_get(4)->get_PageSetup()->get_SectionStart());

// 5 -  在新列上开始下一章节：
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->SetCount(2);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewColumn);
builder->Writeln(u"This text is in section 6.");

ASSERT_EQ(Aspose::Words::SectionStart::NewColumn, doc->get_Sections()->idx_get(5)->get_PageSetup()->get_SectionStart());

doc->Save(get_ArtifactsDir() + u"PageSetup.SetSectionStart.docx");
```


展示如何在文档中添加和删除节。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// 删除文档中的第一个节。
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// 将当前第一个节的副本追加到文档末尾。
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## 另见

* Class [SectionCollection](../../sectioncollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

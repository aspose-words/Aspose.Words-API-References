---
title: "Aspose::Words::Document::get_LastSection 方法"
linktitle: "get_LastSection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_LastSection 方法。获取 C++ 中文档的最后一个节。"
type: docs
weight: 35000
url: /zh/cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


获取文档中的最后一节。

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## 示例



展示如何使用文档生成器创建新节。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 空白文档默认包含一个节，
// 该节包含我们可以编辑的子节点。
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// 使用文档生成器向第一个节添加文本。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// 通过插入节分隔符创建第二个节。
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// 每个节都有其各自的页面设置。
// 我们可以将第二节中的文本拆分为两列。
// 这不会影响第一节中的文本。
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```

## 另见

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

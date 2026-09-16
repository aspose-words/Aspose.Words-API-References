---
title: "Aspose::Words::Section::PrependContent 方法"
linktitle: "PrependContent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Section::PrependContent 方法。在 C++ 中，将源节的内容副本插入到此节的开头。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words/section/prependcontent/
---
## Section::PrependContent method


在此节的开头插入源节内容的副本。

```cpp
void Aspose::Words::Section::PrependContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | 要复制内容的节。 |
## 备注


仅复制源节的 [Body](../get_body/) 内容，页面设置、页眉和页脚不被复制。

如果源节属于不同文档，节点会自动导入。

目标文档中不会创建新节。

## 示例



展示如何将一个节的内容追加到另一个节。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

System::SharedPtr<Aspose::Words::Section> section = doc->get_Sections()->idx_get(2);

ASSERT_EQ(System::String(u"Section 3") + Aspose::Words::ControlChar::SectionBreak(), section->GetText());

// 将第一节的内容插入到第三节的开头。
System::SharedPtr<Aspose::Words::Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// 将第二节的内容插入到第三节的末尾。
System::SharedPtr<Aspose::Words::Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// “PrependContent” 和 “AppendContent” 方法未创建任何新节。
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(System::String(u"Section 1") + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 3" + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 2" + Aspose::Words::ControlChar::SectionBreak(), section->GetText());
```

## 另见

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

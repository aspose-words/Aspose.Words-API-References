---
title: "Aspose::Words::SectionCollection 类"
linktitle: "SectionCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::SectionCollection 类。文档中 Section 对象的集合。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 59000
url: /zh/cpp/aspose.words/sectioncollection/
---
## SectionCollection class


文档中 [Section](../section/) 对象的集合。欲了解更多，请访问 [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) 文档文章。

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 在集合的末尾添加一个节点。 |
| [Clear](../nodecollection/clear/)() | 从此集合和文档中移除所有节点。 |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 确定节点是否在集合中。 |
| [get_Count](../nodecollection/get_count/)() | 获取集合中节点的数量。 |
| [GetEnumerator](../nodecollection/getenumerator/)() override | 提供对节点集合的简单 "foreach" 样式迭代。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 检索给定索引处的节。 |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定节点的从零开始的索引。 |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | 在指定索引处向集合插入一个节点。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 从集合和文档中移除该节点。 |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | 从集合和文档中移除指定索引处的节点。 |
| [ToArray](./toarray/)() | 将集合中的所有节复制到新的节数组中。 |
| static [Type](./type/)() |  |
## 备注


Microsoft Word 文档可以包含多个节。要在 Microsoft Word 中创建节，请选择 Insert/Break 命令并选择分隔类型。该分隔指定节是从新页面开始还是在同一页面继续。

通过编程方式插入和删除节可用于自定义邮件合并期间生成的文档。如果文档需要根据某些条件拥有不同的内容或内容的某些部分，则可以创建一个包含多个节的 \"master\" 文档，并在邮件合并前后删除部分节。

## 示例



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

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

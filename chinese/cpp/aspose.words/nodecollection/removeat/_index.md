---
title: "Aspose::Words::NodeCollection::RemoveAt 方法"
linktitle: "RemoveAt"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeCollection::RemoveAt 方法。在 C++ 中从集合和文档中移除指定索引处的节点。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


从集合和文档中移除指定索引处的节点。

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 节点的零基索引。允许使用负索引，以从列表末尾访问。例如，-1 表示最后一个节点，-2 表示倒数第二个节点，依此类推。 |

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

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

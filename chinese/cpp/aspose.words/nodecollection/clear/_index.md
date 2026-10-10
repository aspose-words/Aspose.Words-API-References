---
title: "Aspose::Words::NodeCollection::Clear 方法"
linktitle: "清除"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeCollection::Clear 方法。 在 C++ 中从此集合和文档中移除所有节点。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


从此集合和文档中移除所有节点。

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## 示例



展示如何从文档中移除所有节。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// 此文档包含一个节，其中有一些子节点，包含并显示文档的全部内容。
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// 清除节的集合，这将移除文档的所有子项。
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
```

## 另见

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

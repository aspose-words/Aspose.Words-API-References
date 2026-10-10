---
title: "Aspose::Words::CompositeNode::get_HasChildNodes 方法"
linktitle: "get_HasChildNodes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CompositeNode::get_HasChildNodes 方法。如果该节点有任何子节点，则返回 true（在 C++ 中）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/compositenode/get_haschildnodes/
---
## CompositeNode::get_HasChildNodes method


如果此节点有任何子节点，则返回 **true**。

```cpp
bool Aspose::Words::CompositeNode::get_HasChildNodes()
```


## 示例



展示如何将两个表的行合并为一个。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// 下面是从文档中获取表的两种方法。
// 1 -  来自 Body 节点的 "Tables" 集合：
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 - 使用 "GetChild" 方法：
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// 将当前表格的所有行追加到下一个表格。
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// 移除空的表格容器。
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## 另见

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

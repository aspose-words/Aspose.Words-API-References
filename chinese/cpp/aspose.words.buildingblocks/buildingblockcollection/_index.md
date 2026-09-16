---
title: "Aspose::Words::BuildingBlocks::BuildingBlockCollection 类"
linktitle: "BuildingBlockCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BuildingBlocks::BuildingBlockCollection 类。文档中 BuildingBlock 对象的集合。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


文档中 [BuildingBlock](../buildingblock/) 对象的集合。要了解更多信息，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class BuildingBlockCollection : public Aspose::Words::NodeCollection
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 在集合的末尾添加一个节点。 |
| [Clear](../../aspose.words/nodecollection/clear/)() | 从此集合和文档中移除所有节点。 |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 确定节点是否在集合中。 |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | 获取集合中节点的数量。 |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | 提供对节点集合的简单 "foreach" 样式迭代。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 检索给定索引处的构建块。 |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定节点的从零开始的索引。 |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | 在指定索引处向集合插入一个节点。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 从集合和文档中移除该节点。 |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | 从集合和文档中移除指定索引处的节点。 |
| [ToArray](./toarray/)() | 将集合中的所有构建块复制到新的构建块数组中。 |
| static [Type](./type/)() |  |
## 备注


您不能直接创建此类的实例。要访问构建块集合，请使用 [BuildingBlocks](../glossarydocument/get_buildingblocks/) 属性。

## 另见

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)

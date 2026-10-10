---
title: "Aspose::Words::NodeCollection::Insert 方法"
linktitle: "Insert"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeCollection::Insert 方法。 在 C++ 中将节点插入到集合的指定索引位置。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/nodecollection/insert/
---
## NodeCollection::Insert method


在指定索引处向集合插入一个节点。

```cpp
void Aspose::Words::NodeCollection::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Node> &node)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 节点的零基索引。允许使用负索引，以从列表末尾访问。例如，-1 表示最后一个节点，-2 表示倒数第二个节点，依此类推。 |
| 节点 | const System::SharedPtr\<Aspose::Words::Node\>\& | 要插入的节点。 |
## 备注


该节点作为子节点插入到创建集合的节点对象中。

如果索引大于或等于 [Count](../get_count/)，则节点将添加到集合的末尾。

如果索引为负且其绝对值大于 [Count](../get_count/)，则节点将添加到集合的末尾。

如果要插入的节点是从另一个文档创建的，您应该使用 [ImportNode()](../) 将节点导入到当前文档。导入后的节点随后可以插入到当前文档中。

## 示例



展示如何使用 [NodeCollection](../)。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用 DocumentBuilder 插入 Run 来向文档添加文本。
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// 每次调用 "Write" 方法都会创建一个新的 Run，
// 随后它会出现在父 Paragraph 的 RunCollection 中。
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// 我们也可以手动将节点插入到 RunCollection 中。
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// 访问各个 Run 并将其移除，以从文档中删除相应的文本。
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## 另见

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

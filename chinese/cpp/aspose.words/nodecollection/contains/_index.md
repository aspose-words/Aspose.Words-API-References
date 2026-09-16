---
title: "Aspose::Words::NodeCollection::Contains 方法"
linktitle: "Contains"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeCollection::Contains 方法。确定节点是否在 C++ 中的集合中。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/nodecollection/contains/
---
## NodeCollection::Contains method


确定节点是否在集合中。

```cpp
bool Aspose::Words::NodeCollection::Contains(const System::SharedPtr<Aspose::Words::Node> &node)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 节点 | const System::SharedPtr\<Aspose::Words::Node\>\& | 要定位的节点。 |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.
## 备注


此方法执行线性搜索；因此，平均执行时间与 [Count](../get_count/) 成正比。

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

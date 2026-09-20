---
title: "Aspose::Words::ParagraphCollection 类"
linktitle: "ParagraphCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphCollection 类。提供对 Paragraph 节点集合的类型化访问。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 48000
url: /zh/cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


提供对 [Paragraph](../paragraph/) 节点集合的类型化访问。要了解更多信息，请访问 [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/) 文档文章。

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | 检索给定索引处的 [Paragraph](../paragraph/)。 |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定节点的从零开始的索引。 |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | 在指定索引处向集合插入一个节点。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 从集合和文档中移除该节点。 |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | 从集合和文档中移除指定索引处的节点。 |
| [ToArray](./toarray/)() | 将集合中的所有段落复制到一个新的段落数组中。 |
| static [Type](./type/)() |  |

## 示例



展示如何检查段落是否为移动修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// 本文档包含“Move”修订，当我们使用光标突出显示文本时会出现这些修订，
// 然后将其拖动以移动到另一个位置
// 在 Microsoft Word 中通过 "Review" -> "Track changes" 跟踪修订。
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// 移动修订由一对 "Move from" 和 "Move to" 修订组成。
// 这些修订是文档的潜在更改，我们可以接受或拒绝它们。
// 在我们接受/拒绝移动修订之前，文档
// 必须跟踪文本的出发和到达位置。
// 第二段和第四段定义了这种修订，因此两者内容相同。
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// "Move from" 修订是我们拖动文本的段落。
// 如果我们接受该修订，此段落将消失，
// 而另一个将保留且不再是修订。
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// "Move to" 修订是我们将文本拖动到的段落。
// 如果我们拒绝该修订，此段落将消失，而另一个将保留。
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## 另见

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

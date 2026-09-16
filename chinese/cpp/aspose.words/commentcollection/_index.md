---
title: "Aspose::Words::CommentCollection class"
linktitle: "CommentCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CommentCollection 类。提供对 Comment 节点集合的类型化访问。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/commentcollection/
---
## CommentCollection class


提供对 [Comment](../comment/) 节点集合的类型化访问。要了解更多，请访问 [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/) 文档文章。

```cpp
class CommentCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | 在给定索引处检索一个 [Comment](../comment/)。 |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定节点的从零开始的索引。 |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | 在指定索引处向集合插入一个节点。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 从集合和文档中移除该节点。 |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | 从集合和文档中移除指定索引处的节点。 |
| [ToArray](../nodecollection/toarray/)() | 将集合中的所有节点复制到一个新的节点数组中。 |
| static [Type](./type/)() |  |

## 示例



展示如何将评论标记为 "done"。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// 插入评论以指出错误。
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// 评论具有一个 "Done" 标志，默认设置为 "false"。
// 如果评论建议我们在文档中进行更改，
// 我们可以应用更改，然后再设置 "Done" 标志以指示已纠正。
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// 已标记为 "done" 的评论会自行区分
// 与未标记为 "done" 的评论使用淡化的文字颜色区分。
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## 另见

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
